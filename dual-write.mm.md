# Dual-Write Strategy in Microservices
- Modular Monolith
  - Service Runtime: Single process
  - Datasources: Single
  - Point of Control: Centralized
  - Steps/Flow execution: At once
  - Properties: ACID/blocking/synchronous
  - Examples: Local transactions
- Two-phase Commit (2PC)
  - Service Runtime: Single/Multiple
  - Datasources: Heterogenerous (require XA)
  - Point of Control: Centralized
  - Steps/Flow execution: At once (for happy paths), highly coupled
  - Properties: ACID/blocking/synchronous
  - Examples: XA, JTA, WS-AT
- Orchestration
  - Service Runtime: Multiple
  - Datasources: Heterogenerous
  - Point of Control: Centralized
  - Steps/Flow execution: Sequential, temporal decoupling
  - Properties: ACD/non-blocking/(a)synchronous
  - Examples: Saga/Outbox, Debezium, Kafka
- Choreography
  - Service Runtime: Multiple
  - Datasources: Heterogenerous
  - Point of Control: Distributed
  - Steps/Flow execution: Sequential, temporal decoupling
  - Properties: ACD/non-blocking/asynchronous
  - Examples: Saga/Outbox, Debezium, Kafka
- Parallel Pipeline
  - Service Runtime: Multiple
  - Datasources: Heterogenerous
  - Point of Control: Distributed
  - Steps/Flow execution: Parallel, temporal decoupling
  - Properties: ACD/non-blocking/asynchronous
  - Examples: Listen to yourself pattern
- Ref: https://www.slideshare.net/bibryam/dual-write-strategies-for-microservices