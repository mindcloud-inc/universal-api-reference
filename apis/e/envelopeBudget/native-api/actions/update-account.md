# Update Account with EnvelopeBudget

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:budget_id/:account_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [Update Account](https://envelopebudget.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budget_id` | path | `string` | yes |
| `account_id` | path | `string` | yes |
| `name` | body | `string` | no |
