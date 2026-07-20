# Create Lead with HirePOS

Creates a new lead in HirePOS.

## Endpoint

- **Method:** `POST`
- **Path:** `/Leads`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Create Lead](https://docs.hirepos.com/en/articles/3907009)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AddressLine1` | body | `string` | no | Primary lead address line. |
| `AddressLine2` | body | `string` | no | Secondary lead address line. |
| `City` | body | `string` | no | Lead city. |
| `Company` | body | `string` | no | Lead company name. |
| `Email` | body | `string` | no | Lead email address. |
| `Fax` | body | `string` | no | Lead fax number. |
| `FirstName` | body | `string` | no | Lead first name. |
| `LastName` | body | `string` | no | Lead last name. |
| `Notes` | body | `string` | no | Additional lead notes. |
| `Phone1` | body | `string` | no | Primary lead phone number. |
| `Phone2` | body | `string` | no | Secondary lead phone number. |
| `Phone3` | body | `string` | no | Third lead phone number. |
| `Postcode` | body | `string` | no | Lead postcode. |
| `State` | body | `string` | no | Lead state. |
