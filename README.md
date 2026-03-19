```mermaid
 sequenceDiagram
participant U as usuario
participant A as app
participant BA as backend
participant B as banco

U->>A: usuario clica e escolhe endereço
note over A: GPS integrado
A->>BA: Endereço(cook,UserID)
note over BA: calcula distancia
BA->>B: buscar Ruas e numeros - UserId
B-->>BA:Endereços
BA-->>A: Historico, Destancia
A-->>U: PesquisaNovos endereços ou Exixtente
