# Benchmark de NL2SQL com foco em Prompt Injection

Este repositório reúne a base de avaliação experimental do TCC, com perguntas legítimas, prompts adversariais, critérios de sucesso e métricas de risco e utilidade para aplicações NL2SQL.

## Objetivo
Avaliar o comportamento de diferentes configurações de segurança em pipelines NL2SQL, medindo redução de risco, impacto na utilidade e capacidade de auditoria.

## Estrutura do benchmark
### Perguntas legítimas
Conjunto de consultas analíticas válidas com ground truth conhecido.

### Suíte adversarial
Prompts maliciosos criados para testar:
- bypass de políticas
- ampliação indevida de escopo
- exfiltração
- DoS lógico
- contorno semântico

### Configurações comparadas
- Config 0: baseline inseguro
- Config 1: somente read-only e bloqueios superficiais
- Config 2: allowlist, escopo e limites
- Config 3: intenção estruturada, validador, políticas, templates e executor auditado

## Métricas principais
### Segurança
- ASR (Attack Success Rate)
- SSR (Scope-Shift Rate)
- Q-DoS Success

### Utilidade
- Acc (Acurácia)
- FBR (False Block Rate)

### Operação
- latência média
- latência p95

### Governança
- audit coverage
- evidence grounding

## Estrutura do repositório
- `dataset/perguntas-legitimas/`
- `dataset/prompts-adversariais/`
- `ground-truth/`
- `metricas/`
- `resultados/`
- `scripts/`

## Finalidade
Oferecer uma base reprodutível para testar o efeito de políticas de segurança em aplicações NL2SQL.

## Status
Em desenvolvimento.
