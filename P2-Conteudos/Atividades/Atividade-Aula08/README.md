# IEC - Atividade Aula 08

## Relatórios de Cobertura & Vulnerabilidade + Badges no README

**Disciplina:** Integração e Entrega Contínua – DSM  
**Professora:** Lucineide  
**Aluno:** Gustavo Silva  
**Semestre:** 1º Semestre / 2026

---

**LINK DA ATIVIDADE**  
https://github.com/GustavoReis-xml/IEC-atividade08

## 📋 Descrição

Este projeto implementa os exercícios da Atividade 8, focados em **relatórios de cobertura de testes**, integração com **Codecov**, e **badges de qualidade** no README. O projeto é baseado no sistema de monitoramento do **INPE** para alertas de queimadas e monitoramento climático.

---

## 📁 Estrutura do Projeto

```
IEC-atividade08/
├── src/
│   ├── alerta.js              # Função classificarAlerta()
│   ├── notificacao.js         # Função enviarNotificacao()
│   ├── processamento.js      # Função processarAlerta() - integração
│   └── monitoramento.js      # Módulo de monitoramento climático (inundações)
├── tests/
│   ├── alerta.test.js         # Testes unitários de alerta
│   ├── integracao.test.js     # Testes de integração
│   ├── processamento.test.js  # Testes de processamento
│   ├── mock.test.js           # Testes com mock
│   ├── erro.test.js           # Testes de simulação de erro
│   └── monitoramento.test.js  # Testes do módulo de monitoramento
├── .github/
│   └── workflows/
│       ├── security.yml       # Workflow de auditoria de segurança
│       └── coverage.yml       # Workflow de cobertura + Codecov
├── codecov.yml                # Configuração do Codecov
├── package.json               # Scripts com test:coverage
├── jest.config.js             # Configuração do Jest com cobertura
├── .gitignore
└── README.md
```

---

## 🚀 Como Executar

### Instalar dependências
```bash
npm install
```

### Rodar os testes
```bash
npm test
```

### Gerar relatório de cobertura (Exercício 1)
```bash
npm run test:coverage
```

---

## 📝 Exercícios Implementados

| Exercício | Descrição | Arquivo |
|-----------|-----------|---------|
| 1 | Comando `test:coverage` no `package.json` | `package.json` |
| 2 | Pipeline de cobertura em PRs para `main` | `.github/workflows/coverage.yml` |
| 3 | Instalação e configuração do Codecov | `codecov.yml` + `jest.config.js` |
| 4 | Pipeline de upload ao Codecov | `.github/workflows/coverage.yml` |
| 5 | Badges de CI e Cobertura no README | `README.md` |

---

## ✅ Resultados dos Testes

- **33 testes** passando com sucesso
- **100% de cobertura** em todos os módulos (Statements, Branches, Functions, Lines)

---

## 📄 Licença

MIT License
