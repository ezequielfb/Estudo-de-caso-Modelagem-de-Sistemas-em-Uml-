🏗️ Documentação de Requisitos: Sistema Pousadas Férias no Norte
Este projeto apresenta a especificação e modelagem UML para um sistema de gestão de hotelaria, focando na automação de reservas, controle de consumo e faturamento.

📋 1. Requisitos Funcionais (RF)
O sistema foi concebido para atender às seguintes capacidades:

Gestão de Reservas (RF01-RF05): Suporte a reservas online (com confirmação via pagamento de diária) e telefônicas (via pré-reserva e validação manual). Inclui fluxos de cancelamento e cadastro obrigatório de clientes.

Gestão Administrativa (RF06, RF07, RF10): Módulos para precificação dinâmica de diárias, catálogo de produtos e manutenção de cadastros (funcionários, unidades e quartos).

Operacional (RF09, RF11): Registro de consumo realizado por atendentes de bares/cozinha e fluxo de checkout com quitação via cartão de crédito.

Integração (RF08): Comunicação com gateway de pagamento externo para processamento de transações.

Business Intelligence (RF12, RF13): Emissão de relatórios de ocupação para níveis gerenciais e administrativos.

📜 2. Regras de Negócio (RN)
Fundamentais para a construção do Diagrama de Classes e Diagrama de Estado:

Capacidade: Limite de 1 a 3 quartos por reserva (RN02).

Política de Depósito: Reservas telefônicas exigem depósito de 40% com prazo de 24h para envio de comprovante (RN03).

Política de Cancelamento: Prazo de 24h para reembolso total; caso contrário, aplica-se multa de uma diária (RN04, RN06).

Horários: Check-in às 15h e Check-out às 12h (RN09).

⚙️ 3. Requisitos Não Funcionais (RNF)
Arquitetura: MVC (Model-View-Controller) (RNF05).

Stack Técnica: Aplicação Web, Java/Hibernate (mapeamento objeto-relacional) e banco de dados MySQL (RNF01-RNF04).

Metodologia: Desenvolvimento ágil utilizando SCRUM (RNF06).

🎨 Modelagem UML Proposta
Para este estudo de caso, os seguintes diagramas foram desenvolvidos:

A. Diagrama de Casos de Uso
Focado na interação entre os Atores (Cliente, Recepção, Atendente de Bar, Administrador e Sistema de Pagamento).

Destaque para o "Extend" no caso de uso de cancelamento e o "Include" na validação de pagamento.

B. Diagrama de Classes
Representação das entidades e seus relacionamentos (1:N, N:M).

Aqui aplicamos as RN01 e RN02 nas cardinalidades entre Cliente, Reserva e Quarto.

C. Diagrama de Sequência (Processo de Checkout)
Detalhamento do fluxo RN08, demonstrando a interação entre o objeto Reserva, Consumo e o Gateway de Pagamento para o fechamento da fatura.

💡 Insight de Engenharia (Visão Futura)
Embora o escopo atual foque em Java e MySQL (RNF02/03), a modelagem UML aqui apresentada foi desenhada de forma agnóstica à linguagem, permitindo uma futura portabilidade para uma arquitetura de microserviços em Python, integrando modelos de IA para predição de ocupação (baseado nos RF12/13).
