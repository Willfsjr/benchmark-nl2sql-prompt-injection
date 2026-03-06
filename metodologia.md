# Metodologia do Benchmark

## Objetivo

Este benchmark tem como finalidade avaliar o comportamento de aplicações NL2SQL sob diferentes níveis de proteção, medindo segurança, utilidade, operação e governança.

## Abordagem

A avaliação compara configurações progressivas de segurança, partindo de um baseline inseguro até uma arquitetura com políticas determinísticas, compilação controlada e execução auditada.

O benchmark é composto por dois conjuntos principais:
- perguntas legítimas, com ground truth previamente definido
- prompts adversariais, com critérios objetivos de sucesso do atacante

## Tipo de pesquisa

Pesquisa aplicada e experimental, com protótipo controlado e avaliação quantitativa.

## Etapas

1. Definir schema mínimo e dataset inicial.
2. Selecionar perguntas legítimas e produzir ground truth.
3. Escrever uma suíte adversarial com ataques variados.
4. Implementar as configurações experimentais.
5. Executar o benchmark e registrar métricas.
6. Comparar segurança, utilidade, latência e auditabilidade.
7. Discutir trade-offs, limites e validade externa.

## Finalidade acadêmica

O benchmark é o núcleo da avaliação do TCC, permitindo quantificar:
- redução de risco
- impacto na utilidade
- custo operacional
- ganho em governança e auditoria
