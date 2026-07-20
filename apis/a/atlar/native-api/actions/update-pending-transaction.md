# Update pending transaction with Atlar

Updates an existing pending transaction in Atlar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/financial-data/v2beta/pending-transactions/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Update pending transaction](https://docs.atlar.com/reference/patch-financial-data-v2beta-pending-transactions-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
