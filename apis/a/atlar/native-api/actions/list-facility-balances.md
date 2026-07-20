# List facility balances with Atlar

Retrieves facility balances from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/facilities/{id}/balances`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List facility balances](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities-id-balances)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `mostRecent` | query | `boolean<string>` | no |
| `localDate` | query | `string<string>` | no |
