# Ponderada - Programação 1 
### Giorgia Rigatti Scherer - T26



## Entrega Mínima

#### A entrega mínima é o que precisa estar presente para a atividade ser considerada: não garante nota máxima.


- Tabela de RNF preenchida para os 8 eixos, com ao menos uma métrica ou critério concreto por eixo
- 3 diagramas de sequência com as 4 camadas (Controller → Service → Repository → Banco), fluxo principal e ao menos 1 fluxo alternativo cada
- Tabela de rastreabilidade (RF → RNF → Diagrama) preenchida para os 3 diagramas


> Critério de qualidade: se o RNF não puder ser testado ou inspecionado, reescreva até que possa.


Rastreabilidade RF → RNF → Sequência


Para cada diagrama entregue, indique quais RFs e RNFs ele cobre


# 1. Introdução 


## Requisitos Não Funcionais - Conectadas aos 8 eixos ISO/EIC 25010

Os requisitos não funcionais (RNFs) descrevem como o sistema deve se comportar em termos de qualidade, complementando os requisitos funcionais. Para sua definição, são considerados os 8 eixos do modelo ISO/IEC 25010, que orientam a avaliação da qualidade de software de forma estruturada.

Dessa forma, os RNFs permitem estabelecer critérios mensuráveis e verificáveis, garantindo que o sistema atenda a aspectos como desempenho, segurança, usabilidade e confiabilidade, além de possibilitar sua validação por meio de testes ou inspeção.



## Tabela de Requistos Não Funcionais (RNF) 

| Eixo | Requisito | Métrica / Critério (Testável) |
|------|----------|------------------------------|
| Usabilidade | RNF01: O sistema deve permitir que o Capataz registre eventos operacionais com baixa carga cognitiva e fluxo contínuo | Registro concluído em no máximo 3 interações obrigatórias, sem navegação entre telas |
| Confiabilidade | RNF02: O sistema deve garantir integridade e consistência dos dados em cenários offline e online | 100% dos registros criados offline devem ser sincronizados exatamente uma vez, sem perda, duplicidade ou inconsistência |
| Desempenho | RNF03: O sistema deve apresentar baixa latência nas operações de consulta e leitura de dados | p95 < 300ms para consultas com até 100 registros, em ambiente com até 10 mil registros |
| Segurança | RNF04: O sistema deve garantir autenticação e autorização baseadas em perfil em todas as operações | 100% das requisições devem passar por validação de autenticação e autorização antes da execução |
| Capacidade | RNF05: O sistema deve suportar múltiplos usuários concorrentes sem degradação significativa de desempenho | Suportar até 50 usuários simultâneos mantendo p95 < 500ms nos endpoints críticos |
| Portabilidade | RNF06: O sistema deve ser compatível com diferentes dispositivos e navegadores utilizados em campo | Compatibilidade com Chrome 120+ (Android) e Safari 17+ (iOS), mantendo funcionamento funcional |
| Manutenibilidade | RNF07: O sistema deve permitir evolução e manutenção com baixo acoplamento entre camadas | 100% das regras de negócio implementadas na camada Service, com separação entre Controller, Service e Repository |
| Compatibilidade | RNF08: O sistema deve operar corretamente em cenários de integração entre armazenamento local e remoto | Sincronização consistente entre dados locais e servidor, com taxa de erro < 1% em operações de sincronização |