# Mapa experimental GWD — Divisões, fluxos e núcleos

**Experimental · V0.1 · 07/11/2026 · Não representa agentes em produção.**

A [Agency Agents](https://github.com/msitarzewski/agency-agents) reúne mais de 230 perfis e 18 divisões documentais na versão consultada. A GWD usará estas divisões como **ontologia de capacidades**, não como lista de agentes ativos. Para executar, cada perfil precisa de um dono humano, manifesto, ferramentas permitidas, versão, teste e aprovação A0–A3.

## Mapa de fluxos e funções

```mermaid
flowchart LR
  subgraph GOV["Governação e controlo"]
   HUMAN["Direção humana"] --> CORE["GWD Ops Core"]
   CORE --> BRAIN["GBrain / AKH / Vault"]
   CORE --> HERMES["Hermes GWD"]
  end
  subgraph INT["Intelligence & Planning"]
   RESEARCH["Research / Academic / GIS"] --> DESIGN["Product / Project Management"]
  end
  subgraph BUILD["Produto & Engenharia"]
   ENGINEERING["Engineering / Security / Testing"] --> EXPERIENCE["Design / Spatial Computing / Game Dev"]
  end
  subgraph GROW["Receita & Relações"]
   MARKETING["Marketing / Paid Media"] --> SALES["Sales / Support"]
  end
  subgraph ADMIN["Administração e especialidades"]
   FINANCE["Finance"] --> SPECIAL["Specialized / Healthcare"]
  end
  subgraph BU["Business Units"]
   ACADEMY["GWD Academy"]
   MEDIA["Media & Growth"]
   SERVICE["Sales & Customer Ops"]
   FUTURE["Commerce / Ventures · candidatas"]
  end
  HERMES --> RESEARCH
  HERMES --> ENGINEERING
  HERMES --> MARKETING
  HERMES --> FINANCE
  RESEARCH --> ACADEMY
  DESIGN --> ACADEMY
  EXPERIENCE --> MEDIA
  MARKETING --> MEDIA
  SALES --> SERVICE
  SPECIAL --> FUTURE
  BU --> OBS["Galaxy 3D / Observatório"]
  OBS -.->|"Evidência sanitizada"| CORE
```

> Este fluxograma é uma **proposta de modelação**, com divisões do Agency Agents agrupadas por afinidade. Não declara competência, acesso, contratação ou execução homologadas.

## Matriz de 18 divisões

| Divisão upstream | Função candidata GWD | Primeiro ensaio |
|---|---|---|
| Academic | Pesquisa e formação | Estrutura de uma aula validada |
| Design | Criativos e experiência | Brief e design QA |
| Engineering | Backend e integrações | API fake e testes |
| Finance | Custos e controlo | Simulação de orçamento |
| Game Development | Gamificação | Protótipo sem utilizadores reais |
| GIS | Análises geoespaciais | Amostra sintética |
| Healthcare | Pesquisa setorial regulada | Documento informativo revisado |
| Marketing | Planeamento comercial | Brief e campanha simulada |
| Paid Media | Anúncios | Rascunho sem publicação ou gasto |
| Product | Propostas de produto | Product brief e critérios de aceite |
| Project Management | Missões e processos | Plano e matriz de riscos |
| Research | Intelligence & fontes | Pesquisa com proveniência |
| Sales | Comercial | Proposta de serviço aprovada |
| Security | Política e isolamento | Teste negativo de acesso |
| Spatial Computing | Galaxy 3D | Constelação sintética |
| Specialized | Especialistas setoriais | Avaliação de domínio |
| Support | Atendimento | Triagem de ticket sintético |
| Testing | Qualidade independente | Regressão e conformidade |

## Fluxo canónico de uma experiência

```mermaid
flowchart TD
 H["Objetivo humano"] --> M["Missão no Ops Core"]
 M --> R{"Risco e mandato?"}
 R -->|A0/A1| P["Pesquisar / preparar rascunho"]
 R -->|A2| S["Executar em escopo reversível"]
 R -->|A3| A{"Aprovação humana autenticada?"}
 A -->|Não| STOP["Bloquear e registar"]
 A -->|Sim| X["Execução autorizada"]
 P --> QA["Revisão e evidência"]
 S --> QA
 X --> QA
 QA --> MEMORY["Aprendizagem proposta ao GBrain"]
 MEMORY -->|Validação| OBS["Galaxy: observado ou simulação"]
```

## Regras de observação

- `CATALOG_CANDIDATE` não equivale a instância ativa.
- `PROPOSED` descreve um papel sem credenciais.
- `TESTING` implica ambiente isolado e dados sintéticos.
- `ACTIVE` exige parecer técnico, aprovação humana e auditoria.
- `RETIRED` significa capacidade descontinuada ou desautorizada.

Os agentes de um cliente não consultam memória ou dados de outro cliente por padrão. A visualização pública receberá só projeções agregadas e aprovadas.

## Da visão à execução

O primeiro caso experimental é **Revenue Now**: Diana coordena o plano, Tomás pesquisa o mercado, Elisa estrutura a oferta e Maia apoia a audiência — com aprovação humana antes de publicação externa, contrato ou despesa. O laboratório medirá custos, qualidade, conversões e entregas reais quando estes dados existirem.
