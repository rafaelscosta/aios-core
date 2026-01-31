# Guia AIOS para Instituto Brasileiro de Cura Pelas Mãos

Este guia explica como usar o sistema AIOS personalizado para o Instituto Brasileiro de Cura Pelas Mãos.

## Visão Geral

O AIOS foi personalizado com **6 agentes especializados** para atender às necessidades específicas de uma escola online de massoterapia:

| Agente | Nome | Especialidade |
|--------|------|---------------|
| `@content-creator` | Maya | Criação de cursos e aulas |
| `@copywriter` | Luna | Copy de vendas e emails |
| `@launch-manager` | Victor | Gestão de lançamentos |
| `@social-media` | Nina | Conteúdo para redes sociais |
| `@automation-engineer` | Theo | Automações e integrações |
| `@student-success` | Sofia | Experiência do aluno |

---

## Quick Start

### 1. Ativar um Agente

Digite o nome do agente para ativá-lo:

```
@copywriter
```

O agente irá se apresentar e mostrar os comandos disponíveis.

### 2. Usar um Comando

Todos os comandos começam com `*`:

```
*create-sales-page
```

O agente irá guiá-lo através do processo com perguntas relevantes.

### 3. Ver Todos os Comandos

```
*help
```

---

## Casos de Uso Comuns

### Lançar um Novo Produto

**Agente:** `@launch-manager` (Victor)

```
@launch-manager
*create-launch-plan
```

Victor irá guiá-lo na criação de:
- Estratégia de lançamento
- Timeline com milestones
- Estrutura do funil
- Checklist de execução

**Workflow completo:** Use `*launch-product` para orquestrar todos os agentes.

---

### Criar um Novo Curso

**Agente:** `@content-creator` (Maya)

```
@content-creator
*create-course-outline
```

Maya irá ajudar a criar:
- Estrutura de módulos
- Roteiros de aulas
- Exercícios práticos
- Materiais de apoio

**Comandos relacionados:**
- `*create-lesson` - Roteiro de aula
- `*create-module` - Módulo completo
- `*create-vsl` - Script de VSL

---

### Escrever Copy de Vendas

**Agente:** `@copywriter` (Luna)

```
@copywriter
*create-sales-page
```

Luna irá criar copy baseada em:
- Seu produto específico
- Público-alvo (massoterapeutas)
- Tom de voz da Natália
- Frameworks de persuasão (AIDA, PAS)

**Comandos relacionados:**
- `*create-email-sequence` - Sequência de emails
- `*create-ad-copy` - Anúncios Meta/Google
- `*create-whatsapp-flow` - Mensagens WhatsApp

---

### Planejar Conteúdo Social

**Agente:** `@social-media` (Nina)

```
@social-media
*create-calendar
```

Nina irá criar:
- Calendário mensal de conteúdo
- Scripts de Reels/TikTok
- Carrosséis para Instagram
- Estratégia de engajamento

**Comandos relacionados:**
- `*create-reels` - Script de Reels
- `*create-carousel` - Carrossel Instagram
- `*research-hashtags` - Pesquisa de hashtags

---

### Configurar Automação

**Agente:** `@automation-engineer` (Theo)

```
@automation-engineer
*create-workflow
```

Theo irá criar:
- Workflows no N8n
- Integrações Hotmart → ActiveCampaign
- Automações WhatsApp
- Configurações de tracking

**Comandos relacionados:**
- `*integrate-hotmart` - Integração Hotmart
- `*integrate-activecampaign` - Integração AC
- `*integrate-whatsapp` - Integração WhatsApp

---

### Melhorar Experiência do Aluno

**Agente:** `@student-success` (Sofia)

```
@student-success
*create-student-journey
```

Sofia irá desenhar:
- Jornada completa do aluno
- Sequência de onboarding
- Estratégia de retenção
- Coleta de depoimentos

**Comandos relacionados:**
- `*create-onboarding` - Boas-vindas
- `*create-testimonial-flow` - Coletar depoimentos
- `*create-graduation` - Cerimônia de formatura

---

## Workflows Completos

### 1. Lançamento de Produto

Ativa múltiplos agentes em sequência para um lançamento completo.

```
@launch-manager
*launch-product
```

**Fases:**
1. Planejamento (Victor)
2. Criação de Conteúdo (Maya, Luna)
3. Setup de Automação (Theo)
4. Pré-lançamento
5. Lançamento
6. Pós-lançamento (Sofia)

### 2. Criação de Curso

```
@content-creator
*create-course
```

**Fases:**
1. Conceito e Planejamento
2. Desenvolvimento de Conteúdo
3. Produção
4. Setup na Plataforma
5. Preparação de Vendas
6. Experiência do Aluno

### 3. Campanha de Conteúdo

```
@social-media
*create-campaign
```

**Fases:**
1. Estratégia
2. Criação de Conteúdo
3. Produção
4. Agendamento
5. Engajamento
6. Análise

---

## Arquivos de Referência

### Dados do Negócio
- `.aios-core/development/data/mcpm-products.md` - Produtos e informações do negócio
- `.aios-core/development/data/mcpm-infrastructure.md` - Stack técnica e integrações

### Templates
- `.aios-core/product/templates/vsl-script-tmpl.yaml` - Template de VSL
- `.aios-core/product/templates/email-sequence-tmpl.yaml` - Template de emails
- `.aios-core/product/templates/lesson-script-tmpl.yaml` - Template de aula

### Configuração de Equipe
- `.aios-core/development/agent-teams/team-mcpm.yaml` - Configuração da equipe

---

## Dicas de Uso

### 1. Seja Específico
Quanto mais contexto você der ao agente, melhor será o resultado.

**Ruim:**
```
*create-email-sequence
```

**Bom:**
```
*create-email-sequence
Produto: Método Cura Pelas Mãos
Objetivo: Lançamento de janeiro
Tipo: PLF com 7 emails
```

### 2. Itere com o Agente
Os agentes fazem perguntas para refinar o resultado. Responda detalhadamente.

### 3. Use Workflows para Projetos Grandes
Para lançamentos ou criação de cursos, use os workflows completos que coordenam múltiplos agentes.

### 4. Mantenha a Voz da Natália
Todos os agentes estão configurados para manter o tom empático, profissional e acolhedor da marca.

---

## Suporte

Se precisar de ajuda com algum agente, use:

```
*guide
```

Cada agente tem um guia detalhado com instruções específicas.

---

*Criado para o Instituto Brasileiro de Cura Pelas Mãos*
