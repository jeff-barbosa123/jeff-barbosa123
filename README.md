<p align="center">
  <img src="./banner.png?v=2" width="100%" />
</p>

<h1 align="center">👋 Olá! Eu sou Jefferson Paulo</h1>
<p align="center">Garantia de Qualidade | Web • Mobile • APIs</p>

---

## 🧾 Resumo executivo
- QA Web/Mobile/API com foco em estratégia de testes, risco e entrega com evidências
- Principais stacks: Cypress, Postman/Insomnia, JMeter, GitHub Actions (CI), Docker (básico)
- Portfólios: [Gestão de Vendas e Clientes](#-projeto-em-foco--gestão-de-vendas-e-clientes-api) | [Akross](#-portfólio-de-qa--akross) | [Acessibilidade QA](#-portfólio-pessoal-de-qa-em-acessibilidade)

## 🧭 Navegação rápida
- [Sobre mim](#-sobre-mim)
- [O que entrego em QA](#-o-que-entrego-em-qa)
- [Tecnologias e Ferramentas](#-tecnologias-e-ferramentas)
- [Gestão de Vendas e Clientes (API)](#-projeto-em-foco--gestão-de-vendas-e-clientes-api)
- [Portfólio Akross](#-portfólio-de-qa--akross)
- [Portfólio Acessibilidade QA](#-portfólio-pessoal-de-qa-em-acessibilidade)
- [Outros projetos](#-outros-projetos-em-qa)
- [Contato](#-contato)

## 🤖 Sobre mim
Profissional de **Qualidade de Software** com experiência em produtos Web e Mobile. Atuo do planejamento ao reporte, cobrindo testes funcionais, integrados, regressão, exploratórios e APIs. Foco em software confiável, seguro e com excelente experiência para o usuário.

- **Formação:** Análise e Desenvolvimento de Sistemas – UNIBRA (2025)
- **Pós-graduação (início):** Fevereiro/2026
- **Objetivo:** Analista de Qualidade de Software em ambientes ágeis, aplicando estratégia de testes, documentação e automação para produtos estáveis e de alta performance.

## 🧭 O que entrego em QA
- Estratégia e plano de testes alinhados ao risco e ao negócio
- Casos e cenários (incluindo BDD) cobrindo fluxos críticos e bordas
- Testes exploratórios com checklist e notas de sessão
- Testes de API com documentação, contract testing e massa de dados
- Regressão focada em releases e smoke tests automatizados
- Evidências claras (prints, logs, vídeos) e reporte objetivo
- Sugestões de UX e melhorias de usabilidade baseadas no comportamento do usuário

## 🛠️ Tecnologias e Ferramentas
- **Testes manuais:** Funcionais, regressão, exploratórios, UAT
- **APIs:** Swagger | Postman | Insomnia
- **Automação:** Cypress (JavaScript) | Node.js | HTML/CSS
- **Performance:** JMeter (carga e smoke de desempenho)
- **CI/CD e colaboração:** Git, GitHub, pipelines, Docker (básico)
- **Gestão ágil:** Jira, Trello, TestRail

## 🚀 Projeto em foco — Gestão de Vendas e Clientes (API)
API REST em evolução para microempreendedores controlarem clientes, produtos e vendas. Criada em um Implementation Day e evoluindo como portfólio com foco em regras de negócio, segurança e qualidade automatizada.

**Status do MVP e foco atual**
- Em andamento: armazenamento em memória (sem persistência ainda)
- Foco: segurança (hash de senhas, rate limiting) e persistência em banco; habilitar pipeline CI/CD
- Qualidade: suíte de testes Mocha/Chai/Supertest; primeiros testes manuais em QA
- Planejamento: backlog público em Issues e board "Gestão de Empreendedores e Faturamento" — https://github.com/users/jeff-barbosa123/projects/6

**Principais entregas do produto**
- Autenticação JWT com bloqueio após 3 tentativas (15 min), expiração por inatividade (30 min) e logout com revogação de tokens
- CRUD de clientes e produtos com validação e e-mail único
- Registro e cancelamento de vendas; faturamento diário, semanal e mensal com filtros por período
- Relatórios exportáveis em CSV, PDF ou Excel; Swagger interativo em /api-docs
- MVP em memória para acelerar iteração e demonstração

**Pilha e arquitetura**
- Node.js 18+, Express, CORS, JWT, Swagger UI, PDFKit, uuid
- Camadas: rotas → controladores → serviços → modelos + middleware (autenticação/erros)
- Swagger: api/resources/swagger.json, servido via /api-docs

**Pontos finais principais**
- Autenticação: POST /api/auth/login, POST /api/auth/logout
- Clientes: GET|POST /api/customers, PUT|DELETE /api/customers/:id
- Produtos: GET|POST /api/products, PUT|DELETE /api/products/:id
- Vendas: GET|POST /api/sales, PUT /api/sales/:id, DELETE /api/sales/:id
- Relatórios: GET /api/reports/revenue, GET /api/reports/revenue/export?format=csv|pdf|excel

**Execução local**
1. Pré-requisitos: Node.js 18+ e npm
2. Clone: `git clone https://github.com/jeff-barbosa123/gestao-vendas-clientes-api.git && cd gestao-vendas-clientes-api`
3. Instale: `npm install`
4. Crie `.env` na raiz (ou `api/.env`):
```
PORT=3000
JWT_SECRET=sua_chave_segura
BASE_URL=http://localhost:3000/api
ADMIN_EMAIL=admin@negocio.com
ADMIN_PASSWORD=admin123
```
5. Desenvolvimento: `npm run dev`  |  Produção/local: `npm start`
6. Base: http://localhost:3000/api  |  Docs: http://localhost:3000/api-docs
7. Credenciais demo: admin@negocio.com / admin123

**Documentação e Garantia de Qualidade**
- Escopo de validação: Documentação/condições de teste.txt
- Plano de Teste (Login): Documentação/Plano_de_Teste_da_Funcionalidade_Login_SGVC.docx
- Plano e Estratégia de Testes (MVP 1.0): Documentação/Plano_e_Estrategia_de_Testes_Adaptada_SGVC(MVP 1.0).docx
- Plano e Estratégia (revisão): Documentação/Plano_e_Estrategia_de_Testes_Adaptada_SGVC.docx e Documentação/Plano_e_Estrategia_de_Testes_Adaptada_SGVC.docx.docx
- Relatórios de sessão:
  - Documentação/Relatório_de_Sessão_Funcionalidade_Login_Empreendedores_SGVC.docx
  - Documentação/Relatório_de_Sessão_Funcionalidade_Cadastro_de_Clientes_Produtos_SGVC.docx
- Testes de API: `npm test` (relatório HTML: `npm run test:report`, saída em api/reports)
- Evidências e planos adicionais: pasta Documentação/

Repositório: https://github.com/jeff-barbosa123/gestao-vendas-clientes-api

## 🧪 Portfólio de QA – Akross
Portfólio de Qualidade para a solução Akross, cobrindo risco, acessibilidade (WCAG 2.1 AA), usabilidade e conformidade. Inclui plano de testes, matriz de risco, auditoria técnica, evidências em vídeo e recomendações acionáveis.

### Akross — Índice interno
- [Visão Geral](#akross--visão-geral)
- [Destaques](#akross--destaques)
- [Entregáveis](#akross--entregáveis)
- [Demonstração](#akross--demonstração)
- [Links Rápidos](#akross--links-rápidos)
- [Guia Rápido](#akross--guia-rápido)
- [Metodologia e Critérios](#akross--metodologia-e-critérios)
- [Ferramentas](#akross--ferramentas)
- [Estrutura](#akross--estrutura)
- [Publicação](#akross--publicação)
- [Contato](#akross--contato)

### Akross — Visão Geral
- Objetivo: aplicar práticas de QA ao produto Akross com foco em risco, acessibilidade e experiência do usuário
- Papel: QA responsável por planejamento, execução, evidências e síntese executiva
- Escopo: testes funcionais, análise de risco, checklist manual WCAG e auditoria técnica
- Público: times de produto/engenharia e stakeholders que precisam de visibilidade de qualidade

### Akross — Destaques
- Fluxo crítico validado e registrado em vídeo completo + versão compacta
- Matriz de riscos priorizada para decisões rápidas
- Auditoria com achados, severidade e recomendações objetivas
- Checklist manual de acessibilidade (WCAG) com apontamentos e próximas ações

### Akross — Entregáveis
- Plano e Estratégia de Testes: `Plano_e_Estrategia_de_Testes_Adaptada_Akoss.docx`
- Foco Corporativo (briefing/objetivos): `Foco_Corporativo_Akoss.docx`
- Estudo de Acessibilidade Manual: `estudo-acessibilidade-manual.docx`
- Relatório de Auditoria: `Relatario_de_Auditoria_Akoss.docx`
- Tabela de Riscos: `Tabela_de_Riscos_Akross.xlsx`
- Evidência em vídeo (compacta): `evidencia_mAFP0cta.mp4`
- Evidência em vídeo (completa): `lighthouse.mp4`
- Evidência de ferramenta (Axe): `AxeDevTools.mp4`

### Akross — Demonstração
- Vídeo compacto: `evidencia_mAFP0cta.mp4`
- Vídeo completo: `lighthouse.mp4`
- Evidência Axe: `AxeDevTools.mp4`

### Akross — Links Rápidos
- Vídeo compacto: `evidencia_mAFP0cta.mp4`
- Vídeo completo: `lighthouse.mp4`
- Evidência Axe: `AxeDevTools.mp4`

### Akross — Guia Rápido
1) Assista `evidencia_mAFP0cta.mp4` (ou `lighthouse.mp4` para o fluxo completo; `AxeDevTools.mp4` para evidência de ferramenta)  
2) Leia `Plano_e_Estrategia_de_Testes_Adaptada_Akoss.docx` para escopo e critérios de aceite  
3) Revise `Tabela_de_Riscos_Akross.xlsx` para a priorização aplicada  
4) Consulte `Relatario_de_Auditoria_Akoss.docx` e `estudo-acessibilidade-manual.docx` para achados e recomendações  
5) Use os vídeos acima para uma visão rápida do fluxo validado

### Akross — Metodologia e Critérios
- Baseado em risco: foco em fluxos críticos e alto impacto
- Acessibilidade: checklist manual (WCAG 2.1 AA) com contraste, navegação por teclado e rótulos
- Evidências: gravação contínua e versionada
- Comunicação: achados com severidade + recomendação acionável por entregável

### Akross — Ferramentas
- Documentação: Word, Excel
- Evidências: ffmpeg portátil (`tools/ffmpeg`) e ScreenToGif
- Versionamento: GitHub

### Akross — Estrutura
```
portfolio-qa-akross/
├─ docs/                         # assets públicos
├─ tools/ffmpeg/                 # ffmpeg portátil
├─ evidencia_mAFP0cta.mp4        # vídeo compacto
├─ lighthouse.mp4                # vídeo completo
├─ AxeDevTools.mp4               # evidência complementar (Axe)
├─ banner-qa-jefferson-paulo.png
├─ Plano_e_Estrategia_de_Testes_Adaptada_Akoss.docx
├─ Foco_Corporativo_Akoss.docx
├─ estudo-acessibilidade-manual.docx
├─ Relatario_de_Auditoria_Akoss.docx
└─ Tabela_de_Riscos_Akross.xlsx
```

### Akross — Publicação
1) Organize os binários: MP4 em `./` (`evidencia_mAFP0cta.mp4`, `lighthouse.mp4`, `AxeDevTools.mp4`)
2) Git LFS (opcional para vídeos maiores): `git lfs track "*.mp4"` e confirme que `.gitattributes` inclui `*.mp4 filter=lfs`
3) Commit (exemplo):
```
git add README.md evidencia_mAFP0cta.mp4 lighthouse.mp4 AxeDevTools.mp4
git commit -m "docs: publicar evidências em vídeo (compacto, completo e Axe)"
```
4) Push: `git push origin main` (ou o branch em uso)
5) Verifique no GitHub se os links de download dos vídeos e documentos abrem corretamente no repositório público

### Akross — Contato
- Jefferson Paulo — LinkedIn | jefferson.p.barbosa23@gmail.com

## 🧪 Portfólio Pessoal de QA em Acessibilidade
Portfólio como Analista de QA focado em acessibilidade digital, unindo estudo manual (WCAG 2.1) e automação E2E com Cypress para um Internet Banking fictício.

### Acessibilidade — Índice interno
- [Visão geral](#acessibilidade--visão-geral)
- [Projetos dentro do portfólio](#acessibilidade--projetos-dentro-do-portfólio)
- [Setup e execução](#acessibilidade--setup-e-execução)
- [Fluxos validados nos testes](#acessibilidade--fluxos-validados-nos-testes)
- [Artefatos gerados](#acessibilidade--artefatos-gerados)
- [Estrutura do repositório](#acessibilidade--estrutura-do-repositório)
- [Boas práticas e próximos passos](#acessibilidade--boas-práticas-e-próximos-passos)

### Acessibilidade — Visão geral
- Objetivo: mostrar um processo completo de QA em acessibilidade — do diagnóstico manual à automação com evidências em vídeo
- Formato: dois projetos integrados (manual + automação) sobre a tela de login em http://localhost:4000
- Escopo: fluxo de login, WCAG 2.1 A/AA, responsividade, navegação por teclado, contraste, tempo de resposta e regressão visual

### Acessibilidade — Projetos dentro do portfólio
- Estudo e documentação manual: PDF `documentacao/estudo-acessibilidade-manual.pdf` com checklist WCAG, heurísticas de Nielsen, severidade e plano de ação
- Automação com Cypress: pasta `banco-web-tests/` com E2E, axe-core, Lighthouse, screenshots de responsividade e vídeos das execuções
- Materiais de apoio: apresentações, GIFs e vídeos na raiz (`assets/`, `videos/`)

### Acessibilidade — Setup e execução
```
# Clonar
git clone https://github.com/jeff-barbosa123/portfolio-acessibilidade-qa.git
cd portfolio-acessibilidade-qa

# Instalar dependências do projeto de testes
cd banco-web-tests
npm install

# Garantir o front em http://localhost:4000 e rodar
npx cypress open        # modo interativo
npx cypress run         # headless (CI)
```
- Cenário específico de login: `npx cypress run --spec "cypress/e2e/login_master.cy.js"`
- Alterar ambiente: `npx cypress run --config baseUrl=https://url-desejada`

### Acessibilidade — Fluxos validados nos testes
- Acessibilidade WCAG 2.1 A/AA com `cy.injectAxe`/`cy.checkA11y`; relatórios JSON/HTML em `cypress/reports`
- Login funcional (usuário `julio.lima` / senha `123456`) validando o componente “Realizar Transferência”
- Responsividade com screenshots por device em `cypress/screenshots/login-*.png`
- Regressão visual com `cy.matchImageSnapshot`
- Navegação por teclado com `cypress-real-events` (Tab/Enter)
- Contraste e legibilidade (impacts serious/critical)
- Desempenho e tempo de resposta; task opcional de Lighthouse (`auditPerformance`)

### Acessibilidade — Artefatos gerados
- `cypress/reports/`: violations-*.json e a11y-report-*.html
- `cypress/screenshots/`: capturas por dispositivo
- `cypress/videos/`: gravações *.mp4 das specs
- `assets/`: banner e GIF para README/apresentações
- `videos/`: `video-de-gravacao-apresentacao.mp4` (demo guiada)

### Acessibilidade — Estrutura do repositório
```
portfolio-acessibilidade-qa/
├─ assets/                      # banner e GIF
├─ banco-web-tests/             # suíte Cypress (código, relatórios, screenshots, vídeos)
├─ documentacao/                # estudo manual e apresentação em PDF
├─ videos/                      # gravação completa da apresentação
└─ README.md
```

### Acessibilidade — Boas práticas e próximos passos
- Pipeline CI para `npx cypress run` e publicação automática de relatórios
- Conectar `saveViolations` a um painel (BI) para acompanhar evolução dos achados WCAG
- Expandir fluxos (cadastro, transferências), testes com leitores de tela e ARIA Live
- Versionar baseline do `cypress-image-snapshot` com atualização controlada

Repositório: https://github.com/jeff-barbosa123/portfolio-acessibilidade-qa

## 🗂️ Outros projetos em QA
**Software para Gestão de Vendas e Clientes (versão anterior)**  
API RESTful com autenticação JWT, cadastro de clientes/produtos, vendas e relatórios.  
_Entregáveis QA:_ estratégia de testes, cenários BDD, regressão por sprint, documentação de API, checklist de release e evidências.  
Repositório: https://github.com/jeff-barbosa123/Software-para-Gest-o-de-Vendas-e-Clientes

**ContaCerta API**  
Sistema financeiro para despesas e relatórios.  
_Entregáveis QA:_ testes exploratórios guiados por charters, cenários de API, checklist de segurança básica, rastreabilidade de requisitos e reportes claros.  
Repositório: https://github.com/jeff-barbosa123/contacerta-api

## 🎯 Como trabalho
- Alinho critérios de aceite e riscos antes de testar
- Crio cenários cobrindo fluxo feliz, bordas e exceções
- Estruturo checklist de regressão por módulo e por release
- Para APIs: coleções versionadas, massa de dados e validação de contratos
- Para automação: seleção de smoke/regressão, page objects simples e relatórios
- Reporto defeitos com passos, dados, logs e sugestão de correção

## 📄 Currículo
[Baixar Currículo (PDF)](./JEFFERSON%20PAULO%20DE%20AGUIAR%20BARBOSA.pdf)

## 📚 Certificações e Estudos
- Participante da **Mentoria Júlio de Lima 2.0 – Testes de Software**
- Estudando automação com Cypress, QA de APIs e boas práticas
- Criando portfólio real com documentos, checklist, cenários e automação

## 📊 Estatísticas GitHub
<p align="center">
  <img height="160em" src="https://github-readme-stats.vercel.app/api?username=jeff-barbosa123&show_icons=true&theme=midnight-purple"/>
  <img height="160em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=jeff-barbosa123&layout=compact&theme=midnight-purple"/>
</p>

## 📫 Contato
Olinda – PE, Brasil  
E-mail: [jeffersonpaulobarbo@gmail.com](mailto:jeffersonpaulobarbo@gmail.com)  
LinkedIn: https://www.linkedin.com/in/jeffersonpaulo-/  
GitHub: https://github.com/jeff-barbosa123

<p align="center">
  Obrigado pela visita! Se quiser conversar sobre QA, tecnologia ou projetos, estou à disposição. 🤝
</p>
