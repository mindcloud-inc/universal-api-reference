# Update loan activity with Atlar

Updates an existing loan activity in Atlar.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/financial-data/v2beta/loans/{loanId}/activities/{id}`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Update loan activity](https://docs.atlar.com/reference/patch-financial-data-v2beta-loans-loanid-activities-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loanId` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
