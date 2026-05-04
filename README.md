# 🎓 AI Study Assistant

Assistente de estudos inteligente criado com n8n que recebe mensagens via Webhook, processa com IA e salva as interações automaticamente.

## 🔄 Como funciona

1. **Receber Mensagem** → Webhook POST recebe a pergunta do aluno
2. **If** → Valida e direciona o fluxo
3. **Assistente de Estudos** → AI Agent (GPT-4o-mini) processa e responde
4. **Memória** → Mantém contexto da conversa
5. **Enviar Respostas** → Retorna a resposta ao aluno
6. **Google Sheets** → Salva todas as interações automaticamente

## 🛠️ Tecnologias

- [n8n](https://n8n.io) — automação de fluxos
- OpenAI GPT-4o-mini — modelo de IA
- Google Sheets — armazenamento de dados

## 👤 Autor

José — projeto desenvolvido para portfólio de automação com IA
