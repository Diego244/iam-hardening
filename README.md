# IAM Hardening (AWS)

## Objetivo
Reduzir privilégios amplos e implementar separação de responsabilidade usando políticas IAM granulares.

## Antes / Depois
| Tipo            | Antes                            | Depois                      |
|-----------------|-----------------------------------|-----------------------------|
| Policies        | permissões amplas (*)             | least privilege por função  |
| MFA             | opcional                          | obrigatório                 |
| Papéis          | genéricos                         | por domínio (ex: BI / ETL)  |

## Evidências
- Políticas antes e depois: `policies/before_overprivileged.json`, `policies/after_least_privilege.json`
- Diagrama de papéis: `docs/roles-map.png`

## O que foi feito
- Divisão de permissões por domínio funcional
- Remoção de permissões “*”
- Criação de políticas específicas

## Próximos passos
- Adicionar IAM Access Analyzer
- Aplicar tags para rastreabilidade de custo

## Licença
MIT
