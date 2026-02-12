# Sistema de Controle de Produção para Fábrica de Plásticos

## Descrição

Este projeto é um sistema web para controle de produção em uma fábrica de plásticos.  
Ele permite gerenciar e monitorar a produção, visualizando relatórios e gráficos baseados em dados reais.

Aplicação em produção: `https://tela-de-login-html.onrender.com`

## Tecnologias Utilizadas

- **Backend (Python/Flask)**: Lógica de negócio, autenticação, rotas e integração com o banco de dados.
- **Flask-SQLAlchemy**: Mapeamento objeto-relacional (ORM) para o banco SQLite.
- **Flask-Login**: Gerenciamento de sessões e autenticação de usuários.
- **Pandas & Plotly**: Tratamento de dados e geração de gráficos.
- **Frontend (HTML, CSS, JavaScript)**: Interface do usuário e interações.
- **Chart.js (via `node_modules`)**: Gráficos no frontend.

## Estrutura de Pastas

- `app.py` — Aplicação Flask principal (rotas, modelos e lógica).
- `templates/` — Páginas HTML (login, registro, dashboard, relatórios, etc.).
- `static/`  
  - `static/style.css`, `static/login.css`, `static/relatorio.css`, etc. — Estilos da interface.  
  - `static/script.js` — Lógica de gráficos usando Chart.js.
- `setup.sql` — Script SQL auxiliar para configuração inicial (se necessário).
- `requirements.txt` — Dependências Python.
- `package.json` / `package-lock.json` — Dependências JavaScript (Chart.js).
- `venv/` — Ambiente virtual Python (ignorado pelo Git).
- `node_modules/` — Dependências JavaScript (ignorado pelo Git).

## Como Rodar o Projeto Localmente

### 1. Pré-requisitos

- **Python 3.10+**
- **Node.js + npm** (apenas se precisar reinstalar o Chart.js)

### 2. Clonar o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd Site-de-Controle-Produtivo
```

### 3. Criar e ativar o ambiente virtual

```bash
python -m venv venv
source venv/bin/activate  # Linux/WSL
# ou, no Windows (PowerShell):
# venv\Scripts\Activate.ps1
```

### 4. Instalar dependências Python

```bash
pip install -r requirements.txt
```

### 5. (Opcional) Instalar dependências JavaScript

```bash
npm install
```

### 6. Executar a aplicação

```bash
python app.py
```

Acesse no navegador: `http://127.0.0.1:5000`

## Funcionalidades Principais

- **Autenticação de Usuários**: Login, registro e controle de sessão.
- **Cadastro de Dados de Produção**: Registro de informações de produção e ocorrências.
- **Consulta com Filtros**: Filtros diários, mensais e por intervalo de datas.
- **Relatórios e Gráficos**: Geração de gráficos usando Plotly (backend) e Chart.js (frontend).

## Boas Práticas e Organização

- Arquivos de código Python concentrados em `app.py` (futuramente podem ser divididos em módulos).
- Arquivos estáticos (`CSS` e `JS`) dentro de `static/`.
- Templates Jinja2 (`HTML`) dentro de `templates/`.
- Arquivos gerados localmente (`venv/`, `node_modules/`, bancos `.db`) são ignorados pelo Git via `.gitignore`.
