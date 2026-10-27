# Service Desk Ticket System

**Sistema de chamados de service desk em Python + SQLite com interface CLI.**

---

## 📋 Visão Geral / Overview

Sistema funcional de gerenciamento de chamados de service desk com interface de linha de comando (CLI). Permite criar, listar e atualizar chamados com prioridade e status. Dados armazenados em banco SQLite local.

Functional service desk ticket management system with command-line interface (CLI). Allows creating, listing, and updating tickets with priority and status. Data stored in local SQLite database.

---

## ⚠️ Aviso / Disclaimer

> **Projeto Pessoal / Laboratório / Personal Project / Laboratory Project**
>
> Este projeto é destinado apenas para fins educacionais e de laboratório. Uso educacional apenas.
>
> This project is for educational and laboratory purposes only.

---

## 📁 Estrutura do Projeto / Project Structure

```
service-desk-ticket-system/
├── src/
│   ├── __init__.py
│   ├── cli.py              # Interface de linha de comando
│   ├── ticket_manager.py   # Gerenciamento de chamados
│   └── models.py           # Modelos de dados e schema
├── tests/
│   ├── __init__.py
│   └── test_ticket_manager.py
├── database/
│   └── .gitignore          # Ignora tickets.db
├── .gitignore
├── README.md
└── requirements.txt
```

---

## 🚀 Instruções de Execução / Execution Instructions

### Pré-requisitos / Prerequisites

- Python 3.8+
- Sem dependências externas

### Executar / Run

```bash
# Iniciar CLI interativa
python -m src.cli

# Ou rodar como módulo principal
python src/cli.py

# Executar testes
python -m unittest discover -s tests -v
```

### Banco de Dados

O banco de dados SQLite (`tickets.db`) é criado automaticamente na primeira execução.
O arquivo é ignorado pelo `.gitignore`.

---

## 📦 Dependências / Dependencies

Nenhuma dependência externa. Usa apenas `sqlite3` e `argparse` da biblioteca padrão.

---

## 📖 Funcionalidades / Features

### Comandos CLI

- `criar` - Criar um novo chamado
- `listar` - Listar todos os chamados
- `listar-status` - Listar chamados por status
- `atualizar` - Atualizar status de um chamado
- `atualizar-prioridade` - Atualizar prioridade de um chamado
- `excluir` - Excluir um chamado
- `status-codes` - Ver códigos de status e prioridade
- `dados-exemplo` - Carregar dados de exemplo

### Status Disponíveis

- `ABERTO` - Chamado aberto
- `EM_ANDAMENTO` - Chamado em andamento
- `RESOLVIDO` - Chamado resolvido
- `FECHADO` - Chamado fechado

### Prioridades

- `BAIXA` - Baixa prioridade
- `MEDIA` - Média prioridade
- `ALTA` - Alta prioridade
- `CRITICA` - Crítica

---

## 🧪 Testes / Tests

Testes unittest para validação de entrada e lógica do sistema.

```bash
python -m unittest discover -s tests -v
```

---

## 🚫 Limitações / Limitations

- Interface apenas em linha de comando (CLI)
- Banco de dados local SQLite (não é escalável para múltiplos usuários simultâneos)
- Sem autenticação ou controle de permissões
- Sem integração com sistemas externos
- Dados de exemplo são fictícios
- Não testado em ambientes de produção

---

## 📝 Licença / License

Projeto pessoal / laboratório. Uso educacional.
