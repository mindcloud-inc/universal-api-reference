# Update forecasted transaction with Atlar

Updates an existing forecasted transaction in Atlar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/analytics/v2beta/forecasted-transactions/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Update forecasted transaction](https://docs.atlar.com/reference/patch-analytics-v2beta-forecasted-transactions-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
