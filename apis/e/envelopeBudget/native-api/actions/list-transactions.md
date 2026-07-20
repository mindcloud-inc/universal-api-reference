# List Transactions with EnvelopeBudget

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions/:budget_id`
- **Base URL:** `https://envelopebudget.com/api`
- **Official documentation:** [List Transactions](https://envelopebudget.com/api/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `budget_id` | path | `string` | yes |
| `account_id` | query | `string` | no |
