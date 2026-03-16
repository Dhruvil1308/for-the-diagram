## Figure 6.1: GuniVox System Workflow

```mermaid
flowchart TD
    A[Data Collection] --> B[Data Cleaning & Processing]
    B --> C[Dataset Storage]
    C --> D[System Integration]
    D --> E[Outbound Call Initiation]
    E --> F[User Voice Input]
    F --> G[Speech Processing]
    G --> H[AI Response Generation]
    H --> I[Voice Response to User]
    I --> J[Call Logging & Analytics]
