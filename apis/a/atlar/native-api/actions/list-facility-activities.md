# List facility activities with Atlar

Retrieves facility activities from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/facilities/{id}/activities`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List facility activities](https://docs.atlar.com/reference/get-financial-data-v2beta-facilities-id-activities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `type` | query | `string<string>` | no |
| `localDate` | query | `string<string>` | no |
| `origin.type` | query | `string<string>` | no |
