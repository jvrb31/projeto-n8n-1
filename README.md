# 🎓 AI Study Assistant — Assistente de Estudos com IA

> Automação inteligente construída com **n8n** que responde perguntas de alunos via Webhook, mantém memória de conversa e salva todas as interações no Google Sheets.

---

## 🚀 Demonstração

> 📸 *[Adicione aqui um print ou GIF do workflow rodando no n8n]*

---

## 💡 O Problema que Resolve

Estudantes frequentemente precisam de respostas rápidas fora do horário de aula. Este projeto automatiza esse suporte com IA, registrando cada interação para análise posterior.

---

## 🔄 Como Funciona

```
[POST /webhook]
      ↓
  Validação (If)
      ↓
  AI Agent (GPT-4o-mini)  ←→  Memória de Conversa
      ↓
  Resposta ao aluno
      ↓
  Google Sheets (log automático)
```

| Etapa | Nó | Função |
|---|---|---|
| 1 | Webhook | Recebe a pergunta via POST |
| 2 | If | Valida e direciona o fluxo |
| 3 | AI Agent | Processa com GPT-4o-mini |
| 4 | Memory | Mantém contexto da conversa |
| 5 | Respond | Retorna resposta ao aluno |
| 6 | Google Sheets | Salva o histórico automaticamente |

---

## 🛠️ Tecnologias

| Ferramenta | Uso |
|---|---|
| [n8n](https://n8n.io) | Orquestração do fluxo |
| OpenAI GPT-4o-mini | Modelo de linguagem |
| Google Sheets | Armazenamento de interações |
| Webhook | Entrada de dados |

---

## ▶️ Como Usar

### Pré-requisitos
- Conta no [n8n.io](https://n8n.io) (cloud ou self-hosted)
- Chave de API da OpenAI
- Conta Google (para o Sheets)

### Instalação

1. Clone este repositório
```bash
git clone https://github.com/jvrb31/projeto-n8n-1.git
```

2. No n8n, vá em **Workflows → Import from file**
3. Importe o arquivo `study-assistant-workflow.json`
4. Configure as credenciais:
   - OpenAI API Key
   - Google Sheets OAuth
5. Ative o workflow e copie a URL do Webhook
6. Envie um POST para testar:
```bash
curl -X POST https://SEU-WEBHOOK-URL \
  -H "Content-Type: application/json" \
  -d '{"message": "O que é machine learning?"}'
```

---

## 📂 Estrutura do Repositório

```
projeto-n8n-1/
├── study-assistant-workflow.json   # Workflow exportado do n8n
└── README.md
```

---

## 👤 Autor

**José** — [LinkedIn](https://linkedin.com/in/josevitorr00) · [GitHub](https://github.com/jvrb31)

> Projeto desenvolvido para portfólio de automação com IA.

**José** — [LinkedIn](https://linkedin.com/in/SEU-LINKEDIN) · [GitHub](https://github.com/jvrb31)

> Projeto desenvolvido para portfólio de automação com IA.
