# Repositório modelo

Arquivos iniciais copiados quando um repositório novo é criado a partir deste modelo. Ruleset, secret scanning e Dependabot não vêm desta cópia. O Terraform aplica isso à parte.

## Regras do repositório

- Apaga a branch depois do merge.
- Permite merge, squash, rebase, auto-merge e atualizar a branch do pull request.
- Issues ligadas. Wiki, Projects e Discussions desligados.
- Em repositório público, secret scanning e push protection ligados.
- Alertas de vulnerabilidade e security updates do Dependabot ligados.

## Ruleset `ruleset-main`

Ativo na branch padrão.

- Não pode apagar a branch.
- Não pode fazer force push.
- Mudança entra por pull request.
- Aprovações exigidas: 0.
- Conversas do review precisam estar resolvidas.
- Merge, squash e rebase liberados.
- Nenhum status check obrigatório. O CodeQL não bloqueia o merge.
- Neste modelo, o admin pode gravar direto na branch padrão, para o Terraform atualizar estes arquivos. Nos repositórios copiados a partir daqui, essa exceção não existe.

Ajuste a linguagem em `.github/workflows/codeql.yml` antes de exigir esse check.
