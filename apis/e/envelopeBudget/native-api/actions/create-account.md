# Create Account with EnvelopeBudget

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:budget_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [Create Account](https://envelopebudget.com/api/docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budget_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `type` | body | `string` | yes |
