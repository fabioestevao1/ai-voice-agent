# 🎙️ AI Voice Agent para Agendamentos

Um agente de voz com inteligência artificial em tempo real, capaz de conversar naturalmente com o usuário e realizar agendamentos em banco de dados sem conflitos de horário.

## 🏗️ Arquitetura

O projeto adota uma estrutura monorepo dividida em três serviços independentes:

*   **`frontend/`**: Interface Web (React) para captura de microfone e conexão com o LiveKit.
*   **`backend-api/`**: API (Node.js) responsável pela autenticação, geração de tokens e regras de negócio/banco de dados.
*   **`agent-worker/`**: Serviço de IA (Node.js + LiveKit Agents) responsável por Speech-to-Text, LLM (Tool Calling) e Text-to-Speech.

## 🚀 Tecnologias Utilizadas
*   **WebRTC/Voz:** [LiveKit](https://livekit.io/)
*   **LLM:** OpenAI GPT-4o / Anthropic Claude 3.5
*   **Backend:** Node.js, Express/NestJS
*   **Frontend:** React / Next.js

## ⚙️ Pré-requisitos
*   Node.js (v18+)
*   Conta no LiveKit Cloud
*   Chaves de API (OpenAI/Anthropic)

## 🛠️ Como rodar localmente

1. Clone o repositório:
\`\`\`bash
git clone https://github.com/SEU_USUARIO/ai-voice-agent.git
cd ai-voice-agent
\`\`\`

2. Instale as dependências e configure as variáveis de ambiente em cada diretório (`frontend`, `backend-api`, `agent-worker`).

# 🎙️ AI Voice Agent for Scheduling

A real-time artificial intelligence voice agent capable of holding natural conversations with users and booking appointments in a database without time conflicts.

## 🏗️ Architecture

This project uses a monorepo structure divided into three independent services:

*   **`frontend/`**: Web interface (React) for microphone capture and connection to the LiveKit room.
*   **`backend-api/`**: Core API (Node.js) responsible for authentication, LiveKit token generation, and database business rules (conflict prevention).
*   **`agent-worker/`**: AI Service (Node.js + LiveKit Agents) responsible for Speech-to-Text, LLM Tool Calling, and Text-to-Speech generation.

## 🚀 Tech Stack
*   **WebRTC / Audio:** [LiveKit](https://livekit.io/)
*   **LLM:** OpenAI GPT-4o / Anthropic Claude 3.5 Sonnet
*   **Backend:** Node.js, Express / NestJS
*   **Frontend:** React / Next.js

## ⚙️ Prerequisites
*   Node.js (v18 or higher)
*   LiveKit Cloud Account (for WebRTC infrastructure)
*   API Keys for your chosen LLM (OpenAI/Anthropic) and TTS provider

## 🛠️ How to Run Locally

Follow these steps to get the three services running on your local machine.

### 1. Clone the repository
\`\`\`bash
git clone https://github.com/YOUR_USERNAME/ai-voice-agent.git
cd ai-voice-agent
\`\`\`

### 2. Configure Environment Variables
In each of the three main folders (`frontend`, `backend-api`, `agent-worker`), duplicate the `.env.example` file, rename it to `.env`, and fill in your API keys and database credentials.

### 3. Install Dependencies & Start Services
You will need three separate terminal windows to run the services simultaneously.

**Terminal 1: Start the Backend API**
\`\`\`bash
cd backend-api
npm install
npm run dev
\`\`\`

**Terminal 2: Start the AI Agent Worker**
\`\`\`bash
cd agent-worker
npm install
npm run dev
\`\`\`

**Terminal 3: Start the Frontend Interface**
\`\`\`bash
cd frontend
npm install
npm run dev
\`\`\`

### 4. Access the Application
Once all services are up, open your browser and navigate to `http://localhost:3000` (or the port specified by your frontend framework) to test the voice agent.