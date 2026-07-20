# Create Transaction with EnvelopeBudget

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/:budget_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [Create Transaction](https://envelopebudget.com/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budget_id` | path | `string` | yes | — |
| `account_id` | body | `string` | no | — |
| `envelope_id` | body | `string` | no | — |
| `payee` | body | `string` | yes | Transaction payee name |
| `date` | body | `string` | no | — |
| `amount` | body | `number` | no | — |
| `memo` | body | `string` | no | — |
