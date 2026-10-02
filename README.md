# study-devsecops.fiap

Laboratório de estudo DevSecOps de ponta a ponta: infraestrutura na Azure com Terraform, aplicação Express em container e esteiras no GitHub Actions com análise de segurança em cada etapa.

## Estrutura

| Pasta | Conteúdo |
|---|---|
| `iac/` | Rede e VM na Azure com Terraform, backend remoto e scripts de autenticação OIDC |
| `app/` | Aplicação Express mínima com proteção CSRF, Dockerfile e script de deploy |
| `.github/workflows/` | Pipelines de pull request e merge para `iac` e `app` |
| `.zap/` | Regras do OWASP ZAP usadas no scan da aplicação |
| `docs/` | Relatórios do ZAP, pesquisa sobre a ferramenta e anotações de estudo |

## Ferramentas

| Ferramenta | Tipo | Onde |
|---|---|---|
| Checkov | SAST de IaC | `iac/` |
| Semgrep | SAST | `app/` |
| OWASP ZAP | DAST | `app/` |
| GHCR | Registro de imagens | `app/` |
