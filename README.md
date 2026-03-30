# 🚀 API Test Automation - ServeRest (Carrefour Technical Challenge)

Projeto de automação de testes de API desenvolvido com **Postman + Newman + GitHub Actions**, com foco em **qualidade, cobertura funcional, cenários negativos e integração contínua (CI/CD)**.

Este projeto foi estruturado com abordagem de **fluxo E2E (Happy Path)** e **cenários negativos independentes**, simulando uma estrutura profissional de testes utilizada em times de QA.

---

## 🛠️ Tecnologias utilizadas

- **Postman**
- **Newman**
- **Node.js**
- **GitHub Actions**
- **JavaScript (Postman Scripts)**

---

## 📂 Estrutura da Collection

A collection foi organizada por fluxo para facilitar execução e manutenção.

```text
01 - Happy Path E2E
02 - Negative Tests - Users
03 - Negative Tests - Login
04 - Negative Tests - Products
05 - Negative Tests - Carts
```

---

## ✅ Cobertura de testes

### 👤 Users
- Criar usuário
- Consultar usuário
- Atualizar usuário
- Excluir usuário
- Validação de campos obrigatórios
- Validação de email inválido
- Validação de ID inválido

### 🔐 Login
- Login com sucesso
- Email inválido
- Password inválido
- Credenciais incorretas

### 🛒 Products
- Criar produto
- Consultar produto
- Preço inválido
- Quantidade inválida
- Duplicidade de produto
- Cenários sem token

### 🛍️ Carts
- Criar carrinho
- Consultar carrinho
- Exclusão de carrinho
- Validação de múltiplos carrinhos
- Cenários sem token

---

## ▶️ Execução local com Newman

### Instalação

```bash
npm install -g newman
npm install -g newman-reporter-htmlextra
```

---

### Executar todos os testes

```bash
newman run Carrefour.postman_collection.json -e carrefour_env.json
```

---

### Executar por suíte

```bash
newman run Carrefour.postman_collection.json -e carrefour_env.json --folder "01 - Happy Path E2E"
```

---

### Gerar relatório HTML

```bash
newman run Carrefour.postman_collection.json -e carrefour_env.json -r cli,htmlextra --reporter-htmlextra-export report.html
```

---

## 🔄 Integração contínua (CI/CD)

O projeto possui pipeline configurado no **GitHub Actions** para execução automática dos testes a cada push.

### Workflow
```text
.github/workflows/api-tests.yml
```

### Execução automática
- Push na branch `master`
- Pull Request

## 📊 Relatório de execução

Os relatórios HTML são gerados automaticamente pelo Newman e disponibilizados como artifact no GitHub Actions.

## 💼 Objetivo do projeto

Este projeto foi desenvolvido com foco em demonstrar habilidades em:

- Testes de contrato
- Automação de API
- Testes E2E
- Testes negativos
- Manipulação de variáveis dinâmicas
- Integração com pipeline CI/CD
- Boas práticas de organização de testes


## 👩‍💻 Karoline Lopes

**Karoline Silva**  
QA Engineer | Software Quality | API Testing | Automation | CI/CD
