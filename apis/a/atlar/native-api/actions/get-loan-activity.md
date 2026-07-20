# Get loan activity with Atlar

Retrieves a loan activity from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/loans/{loanId}/activities/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Get loan activity](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-loanid-activities-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loanId` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
