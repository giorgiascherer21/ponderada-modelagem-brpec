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
| Usabilidade | RNF01: O sistema deve permitir que o Capataz registre uma movimentação com baixa complexidade operacional | Registro concluído em no máximo 3 interações obrigatórias, sem navegação entre telas |
| Confiabilidade | RNF02: O sistema deve garantir integridade dos registros em modo offline e online | 100% dos registros criados offline devem ser sincronizados sem perda, duplicidade ou inconsistência |
| Desempenho | RNF03: O sistema deve apresentar baixa latência nas operações de consulta | p95 < 300ms para consultas com até 100 registros |
| Segurança | RNF04: O sistema deve garantir controle de acesso baseado em perfil de usuário | 100% das requisições devem validar autenticação e autorização antes da execução |
| Capacidade | RNF05: O sistema deve suportar múltiplos usuários simultâneos sem degradação funcional | Suportar até 50 usuários concorrentes mantendo p95 < 500ms |
| Portabilidade | RNF06: O sistema deve ser compatível com diferentes dispositivos e navegadores | Compatível com Chrome 120+ (Android) e Safari 17+ (iOS) |
| Manutenibilidade | RNF07: O sistema deve permitir fácil manutenção e evolução do código | 100% das regras de negócio implementadas na camada Service, com separação entre camadas |
| Confiabilidade | RNF08: O sistema deve garantir recuperação de dados em caso de falha | 100% dos registros locais não sincronizados devem ser recuperáveis após reinicialização |




