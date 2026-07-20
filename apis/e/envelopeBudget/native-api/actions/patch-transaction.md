# Patch Transaction with EnvelopeBudget

## Endpoint

- **Method:** `PATCH`
- **Path:** `/transactions/:budget_id/:transaction_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [Patch Transaction](https://envelopebudget.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budget_id` | path | `string` | yes |
| `transaction_id` | path | `string` | yes |
| `memo` | body | `string` | no |
