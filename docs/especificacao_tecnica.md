# Especificação Técnica de Requisitos

## 1. Requisitos Funcionais (RF)
* **RF01 (Interface de Reserva):** O sistema deve prover interfaces para reservas via Web e via Terminal de Recepção.
* **RF02 (Gestão de Identidade):** Persistência de reservas condicionada ao cadastro prévio do `Hóspede`.
* **RF03 (Gatilho de Pagamento Online):** Transações Web exigem a liquidação imediata de uma diária.
* **RF04 (Workflow Offline):** Reservas telefônicas entram em estado de `Pré-reserva` aguardando validação de depósito bancário pela recepção.
* **RF08 (Integração de Pagamentos):** Comunicação síncrona com API de operadora de cartão de crédito.
* **RF09/11 (Gestão de Faturamento):** Registro de consumo em tempo real e fechamento de conta (Check-out) exclusivamente via cartão.
* **RF12/13 (Business Intelligence):** Geração de relatórios de ocupação para níveis tático (Gerente) e estratégico (Administrativo).

## 2. Regras de Negócio (RN)
* **RN01:** Relação 1:1 entre Reserva e Cliente.
* **RN02:** Uma reserva permite a alocação de 1 a 3 quartos simultâneos.
* **RN03 (Política de Garantia):** Depósito obrigatório de 40% para fluxo telefônico com SLA de 24h para envio de comprovante.
* **RN04/06 (Política de Cancelamento):** Multa de uma diária para cancelamentos feitos com menos de 24h de antecedência.
* **RN09 (Ciclo de Estadia):** Check-in às 15:00h e Check-out às 12:00h.

## 3. Requisitos Não Funcionais (RNF)
* **Plataforma:** Aplicação baseada em tecnologia WEB.
* **Qualidade:** Foco em **Confiabilidade** para a seleção de infraestrutura em nuvem.
* **Processo:** Ciclos de desenvolvimento orientados ao framework Ágil **Scrum**.
