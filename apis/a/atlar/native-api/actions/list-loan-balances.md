# List loan balances with Atlar

Retrieves loan balances from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/financial-data/v2beta/loans/{loanId}/balances`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List loan balances](https://docs.atlar.com/reference/get-financial-data-v2beta-loans-loanid-balances)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `loanId` | path | `string<string>` | yes |
| `mostRecent` | query | `boolean<string>` | no |
| `entityId` | query | `string<string>` | no |
| `localDate` | query | `string<string>` | no |
