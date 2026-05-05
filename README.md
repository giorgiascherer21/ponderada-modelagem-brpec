<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=blur&height=470&color=0:0b3d2e,50:2e8b57,100:7ed957&text=Ponderada%201%20-%20M02&textBg=false&section=header&reversal=true&fontColor=FFFFFF&fontSize=40&fontAlign=50&animation=fadeIn&descAlign=16" alt="Ponderada 1 - M02 Banner" width="550"/>
</p>

# Ponderada 1 - M02

Este repositório reúne a entrega da primeira ponderada de Programação do Módulo 2, desenvolvida no contexto do projeto **PecSync**, proposta do **Grupo 5** em parceria com a **BRPEC**.

O foco da atividade está na definição de requisitos não funcionais verificáveis, na análise dos fluxos principais do sistema por meio de diagramas de sequência UML e na relação desses elementos com a arquitetura em camadas adotada no MVP.

## Conteúdo

- [ponderada.md](/Users/giorgiascherer/ponderada-modelagem-brpec/ponderada.md): documento principal da atividade
- [assets/diagrama_sequencia_1_uml.png](/Users/giorgiascherer/ponderada-modelagem-brpec/assets/diagrama_sequencia_1_uml.png): diagrama 1
- [assets/diagrama_sequencia_2_uml.png](/Users/giorgiascherer/ponderada-modelagem-brpec/assets/diagrama_sequencia_2_uml.png): diagrama 2
- [assets/diagrama_sequencia_3_uml.png](/Users/giorgiascherer/ponderada-modelagem-brpec/assets/diagrama_sequencia_3_uml.png): diagrama 3

## Escopo da atividade

- Requisitos não funcionais com métricas ou critérios verificáveis
- Diagramas de sequência com as camadas `Controller → Service → Repository → Banco`
- Tabela de rastreabilidade `RF → RNF → Diagrama`
- Complemento com constraints e decisões técnicas relacionadas aos fluxos principais

## Projeto de referência

O sistema **PecSync** foi pensado como uma aplicação web **offline-first**, com:

- Front-end em HTML, CSS e JavaScript puro
- Back-end em Node.js
- Persistência local com SQLite
- Foco em integridade, rastreabilidade e sincronização posterior dos dados
