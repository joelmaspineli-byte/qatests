# qatests 
 Sistema Financeiro
Este repositório contém testes automatizados para validação das principais regras de negócio de um sistema financeiro.
O objetivo é garantir a integridade das regras críticas através de uma abordagem baseada na pirâmide de testes.

Regras de Negócio Validadas
 Menor de idade não pode possuir receitas
 Categoria deve respeitar seu tipo (Receita/Despesa/Ambas)
 Exclusão de pessoa remove suas transações (cascata)

 Estratégia de Testes (Pirâmide)
      E2E (Playwright)
      Integração (.NET API)
      Unitários (xUnit)

 Testes Unitários
Validação isolada das regras de negócio
Rápidos e independentes

 Testes de Integração
Testam endpoints da API
Garantem aplicação correta das regras

Testes E2E
Simulam o comportamento do usuário
Validam fluxo completo (UI + API)

Estrutura do Projeto
backend/
frontend/
bugs/
README.md
.NET / C#
xUnit
Playwright

Como Executar
Backend
dotnet test
Frontend
cd frontend-tests
npm install
npx playwright test

Bugs Encontrados
BUG-001 – Menor pode cadastrar receita

Impacto: Alto
Descrição: sistema permite operação inválida
Decisões Técnicas

Foco em regras críticas ao invés de cobertura total

Uso de testes unitários para lógica isolada

Uso de E2E apenas para fluxos essenciais

Estrutura simples e organizada para fácil manutenção



# QA Tests - Financeiro App

##  Estrutura da Pirâmide

- Unitários: validação de regras isoladas
- Integração: API + regras
- E2E: fluxo completo do usuário

##  Como rodar

### Backend
dotnet test

### Frontend
npm install
npm run test

### E2E
npx playwright test

##  Bugs encontrados
- BUG-001: Menor pode ter receita

## Estratégia
Foco em regras críticas:
- Idade
- Categoria
- Exclusão cascata

##  Justificativa
Priorização de regras de negócio ao invés de cobertura superficial.




