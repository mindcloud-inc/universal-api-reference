# List loan activities with Atlar

Retrieves loan activities from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/loans/{loanId}/activities`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List loan activities](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-loanid-activities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loanId` | path | `string<string>` | yes |
| `type` | query | `string<string>` | no |
| `localDate` | query | `string<string>` | no |
| `origin.type` | query | `string<string>` | no |
