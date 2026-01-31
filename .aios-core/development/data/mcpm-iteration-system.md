# Sistema de Iteração e Melhoria de Agentes
# Instituto Brasileiro de Cura Pelas Mãos

## Visão Geral

Este documento define o processo para testar, avaliar e melhorar os agentes AIOS de forma sistemática.

---

## Ciclo de Melhoria

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│    1. TESTAR    →    2. AVALIAR    →    3. REFINAR         │
│        ↑                                      │             │
│        └──────────────────────────────────────┘             │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 1. TESTAR - Cenários de Teste por Agente

### @content-creator (Maya)
| Cenário | Comando | O que testar |
|---------|---------|--------------|
| Criar roteiro de aula | `*create-lesson` | Estrutura, didática, tom |
| Criar VSL | `*create-vsl` | Persuasão, storytelling |
| Criar módulo de curso | `*create-module` | Organização, progressão |

### @copywriter (Luna)
| Cenário | Comando | O que testar |
|---------|---------|--------------|
| Página de vendas | `*create-sales-page` | Headlines, CTAs, objeções |
| Sequência de emails | `*create-email-sequence` | Fluxo, gatilhos, conversão |
| Anúncios | `*create-ad-copy` | Hook, copy curta, CTA |

### @launch-manager (Victor)
| Cenário | Comando | O que testar |
|---------|---------|--------------|
| Plano de lançamento | `*create-launch-plan` | Estratégia, timeline |
| Estrutura de funil | `*create-funnel` | Etapas, conversões |
| Checklist | `*create-checklist` | Completude, ordem |

### @social-media (Nina)
| Cenário | Comando | O que testar |
|---------|---------|--------------|
| Calendário | `*create-calendar` | Frequência, variedade |
| Script de Reels | `*create-reels` | Hook, formato trending |
| Carrossel | `*create-carousel` | Storytelling visual |

### @automation-engineer (Theo)
| Cenário | Comando | O que testar |
|---------|---------|--------------|
| Workflow N8n | `*create-workflow` | Lógica, integrações |
| Integração Hotmart | `*integrate-hotmart` | Eventos, dados |
| Automação WhatsApp | `*create-whatsapp-flow` | Fluxo, mensagens |

### @student-success (Sofia)
| Cenário | Comando | O que testar |
|---------|---------|--------------|
| Jornada do aluno | `*create-student-journey` | Etapas, touchpoints |
| Onboarding | `*create-onboarding` | Acolhimento, clareza |
| Coleta de depoimentos | `*create-testimonial-flow` | Timing, perguntas |

---

## 2. AVALIAR - Template de Feedback

Use este template para documentar cada teste:

```markdown
## Feedback de Teste

**Data:** [data]
**Agente:** [@agente]
**Comando:** [*comando]
**Cenário:** [descrição breve]

### Resultado Geral
- [ ] Excelente - Pronto para uso
- [ ] Bom - Pequenos ajustes
- [ ] Regular - Precisa melhorias
- [ ] Ruim - Retrabalho necessário

### O que funcionou bem
- [ponto positivo 1]
- [ponto positivo 2]

### O que precisa melhorar
- [problema 1]: [sugestão de melhoria]
- [problema 2]: [sugestão de melhoria]

### Exemplos específicos

**Output do agente:**
> [cole aqui um trecho do output]

**O que deveria ser:**
> [como você esperava que fosse]

### Prioridade de correção
- [ ] Alta - Bloqueia uso
- [ ] Média - Importante mas não urgente
- [ ] Baixa - Nice to have
```

---

## 3. REFINAR - Como Instruir Melhorias

### Formato de Solicitação de Melhoria

Para me instruir a fazer melhorias, use este formato:

```
## Melhoria Solicitada

**Agente:** @[nome-do-agente]
**Tipo:** [persona | comando | template | workflow | dados]

### Problema
[Descreva o problema observado]

### Evidência
[Cole exemplos do output problemático]

### Expectativa
[Descreva o que você esperava]

### Sugestão
[Se tiver uma sugestão específica, inclua aqui]
```

### Exemplo Real

```
## Melhoria Solicitada

**Agente:** @copywriter
**Tipo:** template

### Problema
A sequência de emails não inclui emails de carrinho abandonado.

### Evidência
O template email-sequence-tmpl.yaml só tem tipos: launch, nurture, welcome.

### Expectativa
Deveria ter um tipo "cart-abandonment" para recuperar vendas.

### Sugestão
Adicionar tipo com 3-4 emails:
1. Lembrete suave (1h depois)
2. Escassez (24h depois)
3. Última chance (48h depois)
4. Bônus exclusivo (72h depois)
```

---

## Tipos de Melhoria

### 1. Persona
Ajustes na personalidade, tom de voz, ou comportamento do agente.

**Exemplos:**
- "Luna está muito formal, precisa ser mais conversacional"
- "Victor precisa perguntar sobre orçamento antes de sugerir estratégias"

### 2. Comandos
Adicionar, remover ou modificar comandos disponíveis.

**Exemplos:**
- "Adicionar comando *create-stories para Nina"
- "O comando *create-vsl deveria perguntar sobre duração alvo"

### 3. Templates
Melhorar estrutura ou conteúdo dos templates de documentos.

**Exemplos:**
- "Template de VSL precisa de seção para prova social"
- "Adicionar variação de email para Black Friday"

### 4. Workflows
Ajustar fluxos de trabalho e coordenação entre agentes.

**Exemplos:**
- "Lançamento precisa incluir fase de aquecimento de lista"
- "Adicionar checkpoint de aprovação antes de publicar"

### 5. Dados
Atualizar informações de referência do negócio.

**Exemplos:**
- "Adicionar novo produto: Workshop XYZ"
- "Atualizar preços dos produtos"
- "Adicionar novas objeções dos clientes"

---

## Processo Recomendado

### Semana 1-2: Testes Iniciais
1. Teste cada agente com 1-2 cenários
2. Documente feedback usando o template
3. Priorize melhorias

### Semana 3: Primeiro Ciclo de Refinamento
1. Me envie os feedbacks consolidados
2. Implemento as melhorias
3. Você retesta os cenários

### Contínuo: Iteração Gradual
1. Use os agentes no dia a dia
2. Anote problemas quando surgem
3. Consolide melhorias semanalmente
4. Solicite refinamentos em lote

---

## Métricas de Qualidade

### Por Agente
- **Taxa de Aprovação:** % de outputs usáveis sem edição
- **Tempo de Edição:** Quanto tempo leva para ajustar o output
- **Aderência ao Tom:** O output soa como a Natália?

### Por Workflow
- **Completude:** O workflow cobre todas as etapas necessárias?
- **Coordenação:** Os agentes se complementam bem?
- **Tempo Total:** Quanto tempo leva do início ao fim?

---

## Quick Reference: Como Me Pedir Melhorias

### Melhoria Simples
```
Melhoria: @copywriter precisa usar mais emojis nos emails
```

### Melhoria Detalhada
```
Melhoria: @copywriter

Problema: Headlines muito longas
Evidência: "Descubra o método revolucionário que vai transformar..." (15 palavras)
Expectativa: Headlines de 5-8 palavras máximo
Sugestão: Adicionar regra no persona de limite de palavras para headlines
```

### Múltiplas Melhorias
```
Melhorias em lote:

1. @content-creator: Adicionar comando *create-quiz para criar quizzes
2. @copywriter: Template de email precisa campo para emoji no subject
3. @launch-manager: Workflow de lançamento precisa fase de "warm-up"
4. Dados: Adicionar produto "Mentoria VIP" ao catálogo
```

---

## Arquivo de Log de Melhorias

Mantenha um registro das melhorias implementadas:

| Data | Agente | Tipo | Descrição | Status |
|------|--------|------|-----------|--------|
| 2026-01-31 | all | inicial | Criação do squad MCPM | ✅ |
| | | | | |

---

*Use este sistema para evoluir os agentes de forma sistemática e mensurável.*
