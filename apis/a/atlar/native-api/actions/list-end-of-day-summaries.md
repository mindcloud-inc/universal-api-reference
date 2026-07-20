# List end-of-day summaries with Atlar

Retrieves end-of-day summaries from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/accounts/{id}/end-of-day-summaries`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List end-of-day summaries](https://docs.atlar.com/reference/get-financial-data-v2beta-accounts-id-end-of-day-summaries)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `date` | query | `date<string>` | no |
