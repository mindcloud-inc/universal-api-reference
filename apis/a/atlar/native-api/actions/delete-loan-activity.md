# Delete loan activity with Atlar

Deletes an existing loan activity from Atlar.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/financial-data/v2beta/loans/{loanId}/activities/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Delete loan activity](https://docs.atlar.com/reference/delete-financial-data-v2beta-loans-loanid-activities-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loanId` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
