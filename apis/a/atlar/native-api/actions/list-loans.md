# List loans with Atlar

Retrieves loans from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/loans`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List loans](https://docs.atlar.com/reference/get-financial-data-v2beta-loans)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `facilityId` | query | `string<string>` | no |
| `type` | query | `string<string>` | no |
| `closed` | query | `boolean<string>` | no |
| `maturityDate` | query | `string<string>` | no |
