# CONTROCASH

Um sistema de gerenciamento financeiro com funcionalidades de autenticação, transações financeiras, relatórios, investimentos e muito mais.

## Como Contribuir

1. Clone o repositório
2. Crie uma branch para a feature que deseja implementar (ex: `feature/frontend-login`)
3. Faça o commit e envie para o GitHub
4. Abra um Pull Request

Abaixo está a estrutura de Branch e Features que devem ser Seguidos 











Branch (Feature)	            Descrição
feature/backend-auth	        Implementação de autenticação (JWT, login, registro, recuperação de senha)
feature/backend-transactions	CRUD de transações financeiras (receitas e despesas)
feature/backend-reports	        Geração de relatórios financeiros (PDF, CSV)
feature/backend-notifications	Sistema de alertas por e-mail e notificações push
feature/backend-investments	    Cálculo e acompanhamento de investimentos
feature/backend-users	        Gestão de usuários (CRUD, permissões, perfis)
feature/backend-database	    Configuração e otimização do banco de dados
feature/backend-security	    Implementação de segurança (proteção contra ataques, autenticação avançada)
feature/backend-tests	        Testes automatizados (pytest, coverage)



Branch (Feature)	            Descrição
feature/frontend-login	        Tela de login e registro de usuários
feature/frontend-dashboard	    Página principal do painel financeiro
feature/frontend-transactions	Listagem e gerenciamento de transações financeiras
feature/frontend-reports	    Página de relatórios e gráficos financeiros
feature/frontend-notifications	Exibição de notificações no sistema
feature/frontend-investments	Interface para visualizar investimentos
feature/frontend-profile	    Página de edição de perfil do usuário
feature/frontend-settings	    Configurações do sistema (tema, idioma, segurança)
feature/frontend-tests	        Testes automatizados do frontend (Jest, Cypress)




├── backend/  
│   ├── app/  
│   │   ├── api/  
│   │   │   ├── v1/                   # Versão 1 da API  
│   │   │   │   ├── endpoints/        # Rotas separadas por funcionalidade  
│   │   │   │   │   ├── auth.py       # Autenticação e usuários  
│   │   │   │   │   ├── transactions.py # Receitas e despesas  
│   │   │   │   │   ├── reports.py    # Relatórios e dashboards  
│   │   │   │   │   ├── notifications.py # Alertas e notificações  
│   │   │   │   │   ├── investments.py  # Cálculo de investimentos  
│   │   │   │   ├── __init__.py  
│   │   │  
│   │   ├── core/                     # Configurações e inicializações  
│   │   │   ├── config.py              # Configurações do sistema  
│   │   │   ├── security.py            # Segurança (JWT, OAuth)  
│   │   │   ├── database.py            # Conexão com o banco de dados  
│   │   │   ├── __init__.py  
│   │   │  
│   │   ├── models/                    # Definição do banco de dados  
│   │   │   ├── user.py                 # Modelo de usuário  
│   │   │   ├── transaction.py          # Modelo de receitas e despesas  
│   │   │   ├── category.py             # Modelo de categorias  
│   │   │   ├── notification.py         # Modelo de notificações  
│   │   │   ├── investment.py           # Modelo de investimentos  
│   │   │   ├── __init__.py  
│   │   │  
│   │   ├── schemas/                    # Definição de validação de dados (Pydantic)  
│   │   │   ├── user.py                 # Esquema para usuários  
│   │   │   ├── transaction.py          # Esquema para transações  
│   │   │   ├── category.py             # Esquema para categorias  
│   │   │   ├── notification.py         # Esquema para notificações  
│   │   │   ├── investment.py           # Esquema para investimentos  
│   │   │   ├── __init__.py  
│   │   │  
│   │   ├── repositories/               # Camada de acesso ao banco de dados  
│   │   │   ├── user_repository.py      # Funções CRUD de usuários  
│   │   │   ├── transaction_repository.py # Funções CRUD de transações  
│   │   │   ├── category_repository.py  # Funções CRUD de categorias  
│   │   │   ├── investment_repository.py # Funções CRUD de investimentos  
│   │   │   ├── __init__.py  
│   │   │  
│   │   ├── services/                   # Regras de negócio  
│   │   │   ├── user_service.py         # Serviço de usuários  
│   │   │   ├── transaction_service.py  # Serviço de transações  
│   │   │   ├── category_service.py     # Serviço de categorias  
│   │   │   ├── investment_service.py   # Serviço de investimentos  
│   │   │   ├── notification_service.py # Serviço de notificações  
│   │   │   ├── report_service.py       # Serviço de relatórios  
│   │   │   ├── __init__.py  
│   │   │  
│   │   ├── utils/                      # Funções auxiliares  
│   │   │   ├── email.py                # Envio de e-mails  
│   │   │   ├── pdf_generator.py        # Geração de relatórios em PDF  
│   │   │   ├── csv_generator.py        # Geração de relatórios em CSV  
│   │   │   ├── notifications.py        # Funções para envio de notificações  
│   │   │   ├── __init__.py  
│   │   │  
│   │   ├── main.py                     # Ponto de entrada da API  
│   │  
│   ├── tests/                           # Testes automatizados  
│   ├── requirements.txt                 # Dependências do backend  
│   ├── Dockerfile                       # Arquivo para containerização  
│   ├── .env.example                     # Variáveis de ambiente




├── frontend/  
│   ├── public/                          # Arquivos públicos  
│   │   ├── index.html                   # Página inicial  
│   │   ├── favicon.ico  
│   │  
│   ├── src/  
│   │   ├── assets/                      # Ícones, imagens  
│   │   ├── components/                  # Componentes reutilizáveis (botões, gráficos, etc.)  
│   │   ├── pages/                        # Páginas principais  
│   │   │   ├── Home.js                   # Página inicial  
│   │   │   ├── Dashboard.js              # Painel financeiro  
│   │   │   ├── Transactions.js           # Lista de transações  
│   │   │   ├── Login.js                  # Página de login  
│   │   │   ├── Reports.js                # Relatórios financeiros  
│   │   │  
│   │   ├── services/                     # Comunicação com a API backend  
│   │   │   ├── api.js                     # Conexão geral com o backend  
│   │   │   ├── authService.js             # Autenticação e usuários  
│   │   │   ├── transactionService.js      # Transações financeiras  
│   │   │   ├── reportService.js           # Relatórios financeiros  
│   │   │   ├── notificationService.js     # Notificações  
│   │   │  
│   │   ├── styles/                        # Arquivos de estilos (CSS, SASS, Tailwind)  
│   │   │   ├── global.css  
│   │   │   ├── dashboard.css  
│   │   │  
│   │   ├── App.js                         # Componente principal  
│   │   ├── index.js                       # Ponto de entrada  
│   │  
│   ├── package.json                       # Dependências do frontend  
│   ├── vite.config.js                     # Configuração do Vite/Webpack  
│  
├── docs/                                  # Documentação  
│   ├── requisitos.md                      # Requisitos funcionais e não funcionais  
│   ├── arquitetura.md                      # Estrutura do sistema  
│  
├── .gitignore                             # Ignorar arquivos no Git  
├── README.md                              # Documentação do projeto  
├── LICENSE                                # Licença do projeto  















