# Create loan with Atlar

Creates a loan in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/financial-data/v2beta/loans`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create loan](https://docs.atlar.com/reference/post-financial-data-v2beta-loans)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string<string>` | yes |
| `principalAmount` | body | `object<string>` | yes |
| `terms` | body | `object<string>` | yes |
| `lender` | body | `string<string>` | yes |
| `borrower` | body | `string<string>` | yes |
| `startDate` | body | `date<string>` | yes |
| `timezone` | body | `string<string>` | yes |
| `amortizationType` | body | `string<string>` | yes |
