# 🎮 Integração de Provedores de Jogos

<div style="background-color: #f0f7ff; padding: 15px; border-radius: 6px; border-left: 4px solid #3498db; margin-bottom: 20px;">
  <strong>✨ Modernize sua plataforma!</strong> Adicione novos provedores e jogos em minutos com nossa ferramenta de integração.
</div>

## 🌟 Visão Geral

O sistema oferece uma ferramenta completa para integração de novos provedores de jogos diretamente pela interface administrativa, sem a necessidade de desenvolvimento manual de código ou acesso ao servidor. Esta funcionalidade está disponível através do menu **Manutenção > Integração de Jogos**.

<div style="display: flex; justify-content: center; margin: 20px 0;">
  <div style="text-align: center; padding: 15px; max-width: 600px; background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%); border-radius: 10px; color: white;">
    <h3 style="margin-top: 0;">💡 Automatizando o impossível</h3>
    <p>Nossa interface transforma um processo que levaria horas de codificação em apenas alguns cliques!</p>
  </div>
</div>

## 🚀 Funcionalidades Principais

A integração de provedores de jogos permite:

- ✅ **Criação automática** de todas as estruturas necessárias
- ✅ **Definição personalizada** de credenciais para cada provedor
- ✅ **Implementação flexível** da lógica de negócio específica
- ✅ **Monitoramento em tempo real** do processo de integração
- ✅ **Documentação centralizada** das implementações

## 📚 Como Utilizar

### 🔹 Aba Básico

<div style="padding-left: 15px; border-left: 3px solid #4CAF50;">
Nesta aba você configura as informações fundamentais do provedor:

- **📋 Nome do Provedor**: Identificador único no formato CamelCase (ex: NovoProvedor)
- **🔑 Campos de Credenciais**: URL da API, App ID, API Key, Secret Key e campos personalizados
- **🔄 Opção de Migração**: Cria automaticamente as migrações de banco de dados necessárias
</div>

### 🔹 Aba Implementação Avançada

<div style="padding-left: 15px; border-left: 3px solid #FF9800;">
Permite personalizar a lógica de negócio do provedor:

- **🖌️ Editor Visual**: Interface para criar métodos personalizados com validação
- **📤 Upload JSON**: Envio de configurações via arquivo JSON
- **📝 JSON Editor**: Editor de texto para definições complexas
- **📋 Templates de Código**: Exemplos prontos para funções comuns (getBalance, processBet, processWin)
</div>

### 🔹 Aba Logs de Integração

<div style="padding-left: 15px; border-left: 3px solid #2196F3;">
Nova funcionalidade que oferece:

- **📊 Monitoramento em tempo real** do processo de integração
- **🚦 Feedback visual** do status (em andamento, concluído, erro)
- **📜 Logs detalhados** de cada etapa da integração
- **📋 Opção para copiar os logs** para análise ou solução de problemas
</div>

### 🔹 Aba Documentação Detalhada

<div style="padding-left: 15px; border-left: 3px solid #9C27B0;">
Fornece informações completas sobre:

- **📊 Modelos de dados** disponíveis (Wallet, Order, etc.)
- **🔧 Funções auxiliares** para operações comuns
- **📋 Boas práticas** para implementação de webhooks
- **🔄 Processo de integração** com o provedor
</div>

---

## 🏆 Resultado da Integração

<div style="display: flex; justify-content: space-around; flex-wrap: wrap; margin: 20px 0;">
  <div style="width: 180px; margin: 10px; text-align: center; padding: 15px; border-radius: 8px; background-color: #e9f7ef; box-shadow: 0 3px 6px rgba(0,0,0,0.1);">
    <div style="font-size: 2rem;">📄</div>
    <h4 style="margin: 10px 0;">Trait PHP</h4>
    <p style="font-size: 0.8rem;">Lógica de negócio do provedor</p>
  </div>
  <div style="width: 180px; margin: 10px; text-align: center; padding: 15px; border-radius: 8px; background-color: #ebf5fb; box-shadow: 0 3px 6px rgba(0,0,0,0.1);">
    <div style="font-size: 2rem;">🛣️</div>
    <h4 style="margin: 10px 0;">Rotas</h4>
    <p style="font-size: 0.8rem;">Endpoints para webhooks</p>
  </div>
  <div style="width: 180px; margin: 10px; text-align: center; padding: 15px; border-radius: 8px; background-color: #fef5e7; box-shadow: 0 3px 6px rgba(0,0,0,0.1);">
    <div style="font-size: 2rem;">🗄️</div>
    <h4 style="margin: 10px 0;">Migração</h4>
    <p style="font-size: 0.8rem;">Estrutura de banco de dados</p>
  </div>
  <div style="width: 180px; margin: 10px; text-align: center; padding: 15px; border-radius: 8px; background-color: #f4ecf7; box-shadow: 0 3px 6px rgba(0,0,0,0.1);">
    <div style="font-size: 2rem;">🎮</div>
    <h4 style="margin: 10px 0;">GameController</h4>
    <p style="font-size: 0.8rem;">Métodos para exibição dos jogos</p>
  </div>
</div>

## 📋 Próximos Passos

<div style="background-color: #f9f9f9; padding: 15px; border-radius: 6px; margin-bottom: 20px;">
  <h4 style="margin-top: 0;">Após completar a integração:</h4>
  <ol style="margin-bottom: 0;">
    <li>Execute a migração (se criada) via <code>php artisan migrate</code></li>
    <li>Configure as credenciais do provedor em "Chaves dos Jogos" no painel administrativo</li>
    <li>Importe ou cadastre os jogos do provedor</li>
    <li>Configure os webhooks no painel do provedor (quando aplicável)</li>
  </ol>
</div>

## ⚠️ Resolução de Problemas

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 15px; margin-top: 20px;">
  <div style="background-color: #ffebee; padding: 15px; border-radius: 6px; border-left: 4px solid #f44336;">
    <h4 style="margin-top: 0;">🔍 Verificar Logs</h4>
    <p>Consulte os logs em tempo real na aba "Logs de Integração"</p>
  </div>
  <div style="background-color: #e8f5e9; padding: 15px; border-radius: 6px; border-left: 4px solid #4caf50;">
    <h4 style="margin-top: 0;">📚 Consultar Documentação</h4>
    <p>Revise a documentação completa na aba "Documentação Detalhada"</p>
  </div>
  <div style="background-color: #e3f2fd; padding: 15px; border-radius: 6px; border-left: 4px solid #2196f3;">
    <h4 style="margin-top: 0;">🔧 Verificar Dependências</h4>
    <p>Certifique-se de que todas as dependências do sistema estão instaladas</p>
  </div>
  <div style="background-color: #fff8e1; padding: 15px; border-radius: 6px; border-left: 4px solid #ffc107;">
    <h4 style="margin-top: 0;">⚠️ Padrão de Nomenclatura</h4>
    <p>Nomes de provedores devem seguir o padrão CamelCase sem espaços</p>
  </div>
</div>

---

<div style="text-align: center; margin-top: 30px; opacity: 0.8;">
  <p>Desenvolvido pela equipe Fortuna88 🚀</p>
  <p style="font-size: 0.8rem;">Documentação gerada em 2023</p>
</div>
