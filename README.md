# Integração de Jogos

A funcionalidade de Integração de Jogos permite incluir novos provedores de jogos ao sistema a partir do painel administrativo, sem a necessidade de executar comandos no servidor.

## Localização no Painel Administrativo

A ferramenta está disponível em:
```
Admin > Manutenção > Integração de Jogos
```

## Processo de Integração

1. **Nome do Provedor**: Informe o nome do provedor em CamelCase (por exemplo, NovoProvedor).  
2. **Arquivo de Configuração (Opcional)**: Faça o upload de um arquivo JSON com as configurações específicas do provedor.  
3. **Criar Migração**: Se ativado, uma migração será criada para adicionar novos campos ao banco de dados.  
4. **Campos de Credenciais**: Defina as credenciais necessárias para utilizar os serviços do provedor, como URL da API, App ID, API Key, Secret Key e eventuais campos adicionais.  

Após preencher e enviar o formulário, o sistema criará as estruturas necessárias (Trait, Controller, Rota e Migração, se desejado). Em seguida, configure as credenciais do provedor em “Chaves dos Jogos”.

## Recomendações e Observações

1. **Nome do Provedor**: Deve ser em CamelCase e sem espaços, por exemplo “NovoProvedor”.  
2. **Upload JSON (Opcional)**:  
   - Caso possua um arquivo JSON detalhando a configuração (nome, credenciais, endpoints etc.), faça o upload para automatizar a criação das credenciais e demais informações.  
   - Exemplo de conteúdo esperado no JSON (pseudocódigo):
     ```json
     {
       "provider": {
         "name": "NovoProvedor",
         "name_lower": "novoprovedor",
         "description": "Descrição do provedor"
       },
       "credentials": [
         {
           "name": "api_url",
           "type": "url",
           "required": true
         },
         {
           "name": "app_id",
           "type": "text",
           "required": true
         },
         {
           "name": "secret_key",
           "type": "password",
           "required": true
         }
       ],
       "webhooks": [
         "balance",
         "bet",
         "win"
       ],
       "options": {
         "create_migration": true
       }
     }
     ```
3. **Chaves dos Jogos**: Concluída a integração, acesse “Chaves dos Jogos” para inserir os valores reais de cada credencial (API Key, Secret Key, etc.).  
4. **Documentação do Provedor**: Consulte a documentação oficial do provedor para implementar a lógica específica (geração de URLs, webhooks, etc.).  
5. **Pós-Integração**:  
   - Verifique se o nome do provedor aparece na listagem de provedores.  
   - Teste a funcionalidade de criação de jogos e a de webhook para confirmar a comunicação correta com o provedor.  

## Checklist para Conclusão

- [ ] Informar nome do provedor em CamelCase.  
- [ ] (Opcional) Upload de arquivo JSON com as configurações.  
- [ ] Marcar ou não a opção de “Criar Migração”.  
- [ ] Preencher campos de credenciais.  
- [ ] Clicar em “Integrar Provedor”.  
- [ ] Configurar “Chaves dos Jogos” no painel.  
- [ ] Implementar lógica específica na trait gerada, caso necessário.  

Caso ocorram problemas durante a integração, verifique se o nome do provedor está corretamentamente formatado (CamelCase), se as credenciais foram definidas e se o arquivo JSON (quando utilizado) está válido.
