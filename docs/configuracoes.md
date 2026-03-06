# Configurações Experimentais

## Objetivo

Comparar configurações progressivas, com poucas e muitas políticas, para quantificar a redução de risco e o impacto em utilidade.

## Config 0 — Baseline inseguro

- a LLM gera SQL livremente
- o SQL é executado sem mediação robusta
- não há policy engine determinístico
- representa o pior caso de segurança

### Finalidade
Servir como referência para medir o quanto as demais configurações reduzem risco.

## Config 1 — Read-only + bloqueio superficial

- conexão somente leitura no banco
- bloqueio simples de DML/DDL
- uso possível de filtros superficiais, como regex
- ainda sem controle profundo de escopo e estrutura

### Finalidade
Medir o efeito de proteções mínimas e superficiais.

## Config 2 — Allowlist + escopo + limites

- allowlist de tabelas, colunas e views
- escopo obrigatório por papel
- limites de execução, como timeout e limite de linhas
- validação mais forte que a Config 1

### Finalidade
Avaliar o impacto de políticas estruturais e de governança aplicadas antes da execução.

## Config 3 — Arquitetura alvo do TCC

- LLM produz intenção estruturada, como JSON ou AST
- validador e policy engine determinístico
- compilação controlada para SQL por templates
- executor auditado com logging e evidência

### Finalidade
Representa a proposta principal do TCC.

## Resultado esperado

A expectativa é que Config 2 e Config 3 reduzam risco de forma significativa em relação às Configs 0 e 1, com impacto controlado na utilidade.
