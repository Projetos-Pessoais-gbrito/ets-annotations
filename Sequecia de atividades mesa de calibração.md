#### **Semana 1 - Preparação e Desenvolvimento Inicial**

1. **Dia 1 - Interface com Kivy (Layout e Estruturação)**
    
    - Criar a interface gráfica principal com Kivy.
    - Tela de login (Usuário/Admin).
    - Botões de Start, Stop e configurações.
    - Ações condicionais baseadas no tipo de usuário.
2. **Dia 2 - Banco de Dados e Cadastro**
    
    - Implementar banco de dados (SQLite, MySQL, ou outro).
    - Tabelas para armazenar usuários, admins, logs e configurações.
    - Criar funcionalidades de cadastro de Usuário/Admin.
3. **Dia 3 - Funções de Controle para Usuário (Start/Stop)**
    
    - Implementar os botões de start e stop para os usuários.
    - Registrar logs de ações no banco de dados.
    - Testar fluxo de cadastro e funções de usuário.
4. **Dia 4 - Funções de Controle para Admin**
    
    - Permitir que Admins alterem parâmetros do gravador.
    - Incluir funcionalidades avançadas, como assinar firmwares.
    - Atualizar banco de dados com as permissões especiais do Admin.
5. **Dia 5 - Comunicação com a Fonte (Pulsos Elétricos)**
    
    - Estabelecer comunicação com a fonte de alimentação.
    - Implementar envio de pulsos conforme a documentação (240V, 1A).
    - Criar logs de status da fonte.

#### **Semana 2 - Integração e Processos de Firmware**

6. **Dia 6 - Coleta do DevEUI do Microcontrolador**
    
    - Implementar função para coletar o DevEUI e armazenar no banco.
    - Testar coleta de dados em diferentes microcontroladores.
7. **Dia 7 - Envio e Gravação de Firmware (Parte 1)**
    
    - Implementar função para envio do firmware para calibração.
    - Esperar retorno do gravador e armazenar logs do processo.
8. **Dia 8 - Erase do Firmware**
    
    - Implementar a função de `erase` do firmware de acordo com as instruções.
    - Registrar todo o processo e resposta do gravador no banco.
9. **Dia 9 - Envio e Gravação de Firmware (Parte 2 - Gravação Final)**
    
    - Preparar novo firmware com os parâmetros fornecidos.
    - Enviar para o gravador e aguardar a resposta.
    - Registrar logs e status da gravação no banco de dados.
10. **Dia 10 - Geração de Logs Completa**
    
    - Garantir que todos os processos estejam gerando logs detalhados.
    - Implementar função de visualização de logs na interface (Kivy).
11. **Dia 11 - Testes e Integração Final**
    
    - Testar o software completo (cadastro, controles de usuário/admin, pulsos elétricos, gravação de firmware).
    - Ajustar bugs e otimizar o código.
12. **Dia 12 - Entrega e Documentação**
    
    - Finalizar documentação do código.
    - Preparar uma demo ou apresentação do software para validação.

Estrutura de pastas sugerida

src/
│
├── config/                 # Configurações do projeto
│   ├── config.yaml         # Arquivo de configuração (parâmetros, paths, etc.)
│   └── logging_config.py   # Configurações de logging
│
├── data/                   # Armazenamento de dados persistentes (se não usar DB)
│   ├── users.json          # Arquivo JSON para usuários
│   ├── logs/               # Subpasta para arquivos de logs
│   │   └── system.log      # Arquivo de log do sistema
│   └── firmware/           # Subpasta para firmwares
│       └── firmware_v1.bin # Exemplo de firmware binário
│
├── db/                     # Se for usar banco de dados no futuro
│   └── models.py           # Definições do modelo de dados (usando ORM)
│
├── firmware/               # Funções relacionadas ao controle de firmware
│   ├── __init__.py
│   ├── flash.py            # Funções para envio e gravação de firmwares
│   ├── erase.py            # Funções de erase do firmware
│   ├── prepare.py          # Funções de preparação do firmware
│   └── utils.py            # Funções auxiliares relacionadas ao firmware
│
├── hardware/               # Controle de comunicação com hardware (fonte e gravador)
│   ├── __init__.py
│   ├── power_control.py    # Controle da fonte via pulsos elétricos
│   ├── dev_eui.py          # Função de coleta do DevEUI
│   └── serial_comm.py      # Função para comunicação serial (pySerial)
│
├── logs/                   # Módulo para geração e manipulação de logs
│   ├── __init__.py
│   └── logger.py           # Configuração e funções de logging
│
├── ui/                     # Interface de usuário com Kivy
│   ├── __init__.py
│   ├── main.py             # Arquivo principal que inicia o app
│   ├── screens/            # Definição de telas e navegação
│   │   ├── login.kv        # Tela de login
│   │   ├── dashboard.kv    # Tela de controle (Usuário/Admin)
│   │   └── firmware.kv     # Tela para controle de firmware (Admin)
│   └── widgets/            # Componentes de interface reutilizáveis
│       └── custom_button.py# Exemplo de botão customizado
│
├── users/                  # Funções relacionadas a cadastro e autenticação
│   ├── __init__.py
│   ├── auth.py             # Funções de autenticação (login, logout)
│   └── user_manager.py     # Funções de gerenciamento de usuários e admins
│
├── main.py                 # Arquivo principal que inicializa o app
│
├── requirements.txt        # Bibliotecas e dependências do projeto
│
└── README.md               # Documentação do projeto
