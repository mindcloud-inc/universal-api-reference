# List holding activity with Atlar

Retrieves holding activity from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/portfolios/{pid}/holdings/{id}/activities`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List holding activity](https://docs.atlar.com/reference/get-financial-data-v2beta-portfolios-pid-holdings-id-activities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pid` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `type` | query | `string<string>` | no |
| `date` | query | `string<string>` | no |
