# List balances with Atlar

Retrieves balances from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2/accounts/{id}/balances`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List balances](https://docs.atlar.com/reference/get-financial-data-v2-accounts-id-balances)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `type` | query | `string<string>` | no |
| `mostRecent` | query | `boolean<string>` | no |
