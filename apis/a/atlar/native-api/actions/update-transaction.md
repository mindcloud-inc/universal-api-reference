# Update transaction with Atlar

Updates an existing transaction in Atlar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/financial-data/v2/transactions/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Update transaction](https://docs.atlar.com/reference/patch-financial-data-v2-transactions-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
