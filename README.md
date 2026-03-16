<h2 align="center">📞 GuniVox Voice Agent – System Workflow</h2>

<p align="center">
AI Powered Automated Admission Calling System
</p>

---

## 🎯 Workflow Overview

The following diagram explains how GuniVox automates outbound admission calls using  
Twilio, Deepgram STT, LLM decision engine, and Piper TTS.

---

```mermaid
flowchart LR

%% ================= ADMIN =================
subgraph ADMIN PANEL
A[Admin Uploads Leads<br>CSV / Database]
O[Admin Views Analytics<br>Reports & Followups]
end

%% ================= BACKEND =================
subgraph AI CALL ENGINE
B[FastAPI Backend Server]
G[Conversation Intelligence<br>LLM Decision Engine]
H[Admission Knowledge Base<br>Student Database]
M[Conversation Logs<br>Lead Status Storage]
N[Analytics Engine<br>Insights Generator]
end

%% ================= CALL SYSTEM =================
subgraph VOICE PIPELINE
C[Twilio Outbound Call API]
D[Call Connected<br>Student Answers]
E[Real-time Audio Streaming]
F[Speech to Text<br>Deepgram STT]
I[Dynamic Response<br>Generation]
J[Text to Speech<br>Piper TTS]
K[Voice Stream<br>Back to Student]
end

%% ================= FLOW =================
A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H
H --> I
I --> J
J --> K
K --> D

D -->|Call Ends| M
M --> N
N --> O
