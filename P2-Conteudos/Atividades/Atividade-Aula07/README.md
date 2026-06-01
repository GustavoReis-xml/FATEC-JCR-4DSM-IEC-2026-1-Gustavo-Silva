# IEC - Atividade Aula 07

## Introdução a Testes Automatizados Avançados

**Disciplina:** Integração e Entrega Contínua – DSM  
**Professora:** Lucineide  
**Aluno:** Gustavo Silva  
**Semestre:** 1º Semestre / 2026

---

## 📋 Descrição

Este projeto implementa os exercícios da Atividade 7, focados em testes automatizados avançados utilizando **Jest**, auditoria de segurança com **npm audit**, e automação com **GitHub Actions**.

---

## 📁 Estrutura do Projeto

```
IEC-atividade07/
├── src/
│   ├── alerta.js              # Função classificarAlerta()
│   ├── notificacao.js         # Função enviarNotificacao()
│   └── processamento.js      # Função processarAlerta() - integração
├── tests/
│   ├── alerta.test.js         # Exercício 6 - Teste unitário
│   ├── integracao.test.js     # Exercício 7 - Teste de integração
│   ├── processamento.test.js  # Exercício 1 - Teste de integração completo
│   ├── mock.test.js           # Exercício 2 - Mock de função externa
│   └── erro.test.js           # Exercício 8 - Simulação de erro
├── .github/
│   └── workflows/
│       └── security.yml       # Exercício 4 - Workflow de segurança
├── package.json
├── jest.config.js
└── README.md
```

---

## 🚀 Como Executar

### Instalar dependências
```bash
npm install
```

### Rodar os testes (Exercícios 1, 2, 6, 7, 8)
```bash
npm test
```

### Gerar relatório de cobertura (Exercício 9)
```bash
npm test -- --coverage
```

### Auditoria de segurança (Exercício 3)
```bash
npm audit
npm audit fix
```

---

## 📝 Exercícios Implementados

### Exercício 1 - Teste de Integração Completo
Arquivo: `tests/processamento.test.js`  
Valida a execução conjunta de `classificarAlerta()` + `enviarNotificacao()` através da função `processarAlerta()`.

### Exercício 2 - Mock de Função Externa
Arquivo: `tests/mock.test.js`  
Cria mock com `jest.fn()` para simular chamadas a APIs externas.

### Exercício 3 - Verificação de Segurança
Execução de `npm audit` no terminal para verificar vulnerabilidades nas dependências.

### Exercício 4 - Workflow de Segurança
Arquivo: `.github/workflows/security.yml`  
Automatiza auditoria de dependências e execução de testes via GitHub Actions.

### Exercício 5 - Commit e PR
Criação de branch `feature/seguranca`, commit dos arquivos e abertura de PR para `dev`.

### Exercício 6 - Teste Unitário
Arquivo: `tests/alerta.test.js`  
Testes isolados para a função `classificarAlerta()` cobrindo todos os níveis (Crítico, Alto, Médio, Baixo).

### Exercício 7 - Teste de Integração
Arquivo: `tests/integracao.test.js`  
Valida a combinação de `classificarAlerta()` + `enviarNotificacao()` em cenários diversos.

### Exercício 8 - Simulação de Erro
Arquivo: `tests/erro.test.js`  
Demonstra como um valor esperado incorreto gera falha no Jest, e apresenta a correção.

### Exercício 9 - Relatório de Cobertura
Execução de `npm test -- --coverage` para medir a qualidade e abrangência dos testes.

### Exercício 10 - Commit e PR com Testes
Commit dos novos testes e abertura de PR de `feature/testes` para `dev`, acompanhando o pipeline no GitHub Actions.

---

## ✅ Resultados dos Testes

Todos os testes passam com sucesso ao executar `npm test`.

---

## 🔒 Segurança

O workflow de segurança em `.github/workflows/security.yml` executa automaticamente em pushes e pull requests para as branches `dev` e `main`, realizando:
- Auditoria de dependências (`npm audit`)
- Execução de testes (`npm test`)
- Relatório de cobertura (`npm test -- --coverage`)
