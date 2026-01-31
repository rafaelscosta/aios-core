# Instituto Brasileiro de Cura Pelas Mãos - Infraestrutura Técnica

## Visão Geral da Stack

```
┌─────────────────────────────────────────────────────────────────┐
│                        CAMADA DE TRÁFEGO                         │
│  Meta Ads │ Google Ads │ Orgânico (Instagram, YouTube, TikTok)  │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                      CAMADA DE CAPTURA                          │
│      Landing Pages │ Typebot │ Manychat │ Forms                 │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                     CAMADA DE AUTOMAÇÃO                         │
│            N8n │ ActiveCampaign │ Evolution API                 │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                       CAMADA DE VENDAS                          │
│                    Hotmart │ Checkout                           │
└─────────────────────────────────────────────────────────────────┘
                                │
                                ▼
┌─────────────────────────────────────────────────────────────────┐
│                      CAMADA DE ENTREGA                          │
│              Hotmart Club │ Área de Membros                     │
└─────────────────────────────────────────────────────────────────┘
```

---

## Ferramentas por Categoria

### Automação e Integração

#### N8n (Self-hosted)
- **URL:** https://n8n.nataliatanaka.com.br
- **Hospedagem:** VPS Hostinger
- **Uso:** Automações centrais, integrações entre plataformas
- **Workflows principais:**
  - Hotmart → ActiveCampaign (tags de compra)
  - WhatsApp → CRM (captura de leads)
  - Formulários → ActiveCampaign + WhatsApp
  - Abandono de carrinho
  - Notificações internas

#### ActiveCampaign
- **URL:** https://nataliatanaka.activehosted.com
- **Uso:** Email marketing, automações, CRM
- **Integrações:**
  - Hotmart (via N8n)
  - Typebot
  - Landing pages

#### Evolution API
- **URL:** https://evoapi.nataliatanaka.com.br
- **Uso:** WhatsApp Business API
- **Integrações:**
  - N8n
  - Typebot
  - ActiveCampaign

---

### Marketing e Vendas

#### Hotmart
- **URL:** https://hotmart.com
- **Uso:** Plataforma de vendas e entrega de produtos
- **Produtos hospedados:**
  - Todos os cursos
  - Manuais/e-books
  - Mentorias
- **Integrações:**
  - Webhooks para N8n
  - Pixel do Facebook
  - Google Analytics

#### Funnelytics
- **URL:** https://app.funnelytics.io
- **Uso:** Visualização e análise de funis
- **Aplicações:**
  - Mapeamento de funis de lançamento
  - Análise de conversão
  - Planejamento estratégico

---

### Chatbots e Conversação

#### Typebot
- **URL:** https://app.typebot.io
- **Uso:** Chatbots para captura e qualificação
- **Aplicações:**
  - Quiz de qualificação
  - Captura de leads
  - Suporte automatizado
- **Integrações:**
  - N8n (webhooks)
  - ActiveCampaign

#### Manychat
- **URL:** https://manychat.com
- **Uso:** Automação Instagram/Facebook Messenger
- **Aplicações:**
  - Resposta automática no Instagram
  - Captura de leads via DM
  - Fluxos de engajamento

---

### Mídia e Conteúdo

#### Streamyard
- **Uso:** Lives e webinars
- **Integrações:**
  - YouTube Live
  - Facebook Live
  - Instagram Live

#### WebinarKit
- **Uso:** Webinars automatizados
- **Aplicações:**
  - Webinars evergreen
  - Lançamentos

#### HeyGen
- **URL:** https://app.heygen.com
- **Uso:** Vídeos com avatar IA
- **Aplicações:**
  - Vídeos de boas-vindas
  - Conteúdo escalável

#### ElevenLabs
- **URL:** https://elevenlabs.io
- **Uso:** Síntese de voz IA
- **Aplicações:**
  - Narração de conteúdo
  - Audiobooks

---

### Analytics e Tracking

#### Google Analytics
- **Uso:** Analytics principal
- **Configuração:**
  - GA4
  - Enhanced ecommerce
  - Eventos personalizados

#### Google Tag Manager
- **Uso:** Gerenciamento de tags
- **Tags ativas:**
  - Facebook Pixel
  - Google Ads
  - Hotjar
  - Analytics

#### Stape
- **Uso:** Server-side tracking
- **Aplicações:**
  - Bypass de bloqueadores
  - Dados mais precisos
  - CAPI do Facebook

---

### IA e Processamento

#### OpenAI API
- **URL:** https://platform.openai.com
- **Uso:** Automações com IA
- **Aplicações via N8n:**
  - Classificação de mensagens
  - Respostas automáticas
  - Geração de conteúdo

#### Claude AI
- **Uso:** Assistência e criação de conteúdo
- **Aplicações:**
  - Copy
  - Estratégia
  - Análise

#### Deepgram
- **URL:** https://console.deepgram.com
- **Uso:** Transcrição de áudio
- **Aplicações:**
  - Transcrição de aulas
  - Legendas automáticas

#### Qdrant
- **URL:** https://cloud.qdrant.io
- **Uso:** Vector database
- **Aplicações:**
  - RAG para chatbots
  - Busca semântica

#### Redis
- **URL:** https://cloud.redis.io
- **Uso:** Cache e sessões
- **Aplicações:**
  - Cache de automações
  - Rate limiting

---

### Gestão de Projetos

#### ClickUp
- **URL:** https://app.clickup.com
- **Workspace:** HotSales
- **Uso:** Gestão de tarefas e projetos
- **Estrutura:**
  - Espaços por área (Marketing, Conteúdo, etc.)
  - Listas por projeto
  - Automações internas

---

### Hospedagem e DNS

#### Hostinger
- **Tipos:**
  - Compartilhada: Sites WordPress
  - VPS: N8n, Evolution API
- **URL:** https://auth.hostinger.com/br/login

#### Cloudflare
- **URL:** https://dash.cloudflare.com
- **Uso:**
  - DNS
  - SSL
  - CDN
  - Proteção DDoS

---

## Integrações Principais (N8n Workflows)

### 1. Compra no Hotmart → Onboarding
```
Webhook Hotmart → Verificar produto →
ActiveCampaign (tag) → WhatsApp (boas-vindas) →
ClickUp (criar tarefa de acompanhamento)
```

### 2. Lead Capturado → Nutrição
```
Typebot/Form → N8n → ActiveCampaign (adicionar lista) →
WhatsApp (mensagem inicial) → Sequência de emails
```

### 3. Abandono de Carrinho
```
Hotmart webhook (abandono) → Espera 1h →
WhatsApp (lembrete) → Espera 24h →
Email (recuperação) → Espera 48h →
WhatsApp (última chance)
```

### 4. Mensagem WhatsApp → Classificação
```
Evolution API (mensagem recebida) → N8n →
OpenAI (classificar intenção) →
IF dúvida → Resposta automática
IF interesse → Tag + notificar vendedor
IF suporte → Criar ticket
```

---

## Credenciais e Acessos

> **IMPORTANTE:** Nunca armazenar credenciais diretamente no código.
> Usar variáveis de ambiente ou gerenciador de secrets.

### Variáveis de Ambiente Necessárias

```env
# ActiveCampaign
ACTIVECAMPAIGN_URL=https://nataliatanaka.activehosted.com
ACTIVECAMPAIGN_API_KEY=

# Hotmart
HOTMART_TOKEN=
HOTMART_SECRET=

# Evolution API
EVOLUTION_API_URL=https://evoapi.nataliatanaka.com.br
EVOLUTION_API_KEY=

# OpenAI
OPENAI_API_KEY=

# N8n
N8N_WEBHOOK_URL=https://n8n.nataliatanaka.com.br/webhook/

# ClickUp
CLICKUP_API_KEY=
CLICKUP_WORKSPACE_ID=
```

---

## Checklist de Setup para Novos Projetos

### Tracking
- [ ] Pixel do Facebook instalado
- [ ] Google Analytics configurado
- [ ] GTM publicado
- [ ] Eventos de conversão configurados

### Automação
- [ ] Webhook do Hotmart configurado
- [ ] Sequência de onboarding ativa
- [ ] WhatsApp de boas-vindas configurado
- [ ] Tags de segmentação criadas

### Integrações
- [ ] N8n workflows testados
- [ ] ActiveCampaign automações ativas
- [ ] Typebot/chatbot funcional

---

*Documento de referência técnica para o agente @automation-engineer (Theo)*
