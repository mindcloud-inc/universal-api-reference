# Create loan activity with Atlar

Creates a loan activity in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/financial-data/v2beta/loans/{loanId}/activities`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create loan activity](https://docs.atlar.com/reference/post-financial-data-v2beta-loans-loanid-activities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loanId` | path | `string<string>` | yes |
| `type` | body | `string<string>` | yes |
| `amount` | body | `object<string>` | yes |
| `localDate` | body | `date<string>` | yes |
