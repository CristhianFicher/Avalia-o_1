# Workflow  Página Startup

Este documento define as regras de **workflow** e **convenção de commits** adotadas pelo time no desenvolvimento da **Página de Startup**.

---

## Modelo de Workflow

Adotaremos uma **variação simplificada do Git Flow**, com foco em organização e agilidade para o desenvolvimento web.

Branches principais:
- **main** → Versão estável da aplicação (deploy).
- **develop** → Integração contínua das funcionalidades antes de irem para produção.
- **feature/** → Novas seções ou funcionalidades.
- **hotfix/** → Correções de bugs em produção.
- **release/** → Preparação de versões estáveis (pré).

---

## Estratégia de Branches

- **Origem e destino dos merges**:
  - `feature/*` → merge em `develop`
  - `release/*` → merge em `main` (e volta para `develop`)
  - `hotfix/*` → merge em `main` (e volta para `develop`)

- **Exemplos de branches**:
  - `feature/servicos`
  - `feature/portfolio`
  - `feature/depoimentos`
  - `hotfix/css-broken-layout`
  - `release/v1.0.0`

---

## Regras de Atualização

- A branch **main** só recebe merges de `release/*` ou `hotfix/*`.  
- Cada **feature** deve ser desenvolvida em sua própria branch.  
- Todo merge é feito via **Pull Request**. 
- O **deploy automático** (CI/CD) será configurado para rodar a partir da branch `main`.

---

## Política de Revisão e Integração

- Nenhum commit direto em `main` ou `develop`.  
- **Pull Requests** devem incluir:
  - Descrição clara do que foi implementado. 
  - Commits seguindo o padrão semântico.  
- Revisores verificam:
  - Clareza do código (HTML/CSS).  
  - Responsividade e acessibilidade.  
  - Que a seção não quebrou outras partes do site.

---

## Convenção de Commits

Adotaremos o padrão **semântico**, com a sintaxe:

