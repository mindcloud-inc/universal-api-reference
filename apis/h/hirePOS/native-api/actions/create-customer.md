# Create Customer with HirePOS

Creates a new customer in HirePOS.

## Endpoint

- **Method:** `POST`
- **Path:** `/Customers`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [Create Customer](https://docs.hirepos.com/en/articles/2314561)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `AddressLine1` | body | `string` | no | Primary customer address line. |
| `AddressLine2` | body | `string` | no | Secondary customer address line. |
| `City` | body | `string` | no | Customer city. |
| `Company` | body | `string` | no | Customer company name. |
| `Country` | body | `string` | no | Customer country. |
| `Email` | body | `string` | no | Customer email address. |
| `Fax` | body | `string` | no | Customer fax number. |
| `FirstName` | body | `string` | no | Customer first name. |
| `IsMobile1` | body | `boolean` | no | Whether Phone 1 is a mobile number. |
| `IsMobile2` | body | `boolean` | no | Whether Phone 2 is a mobile number. |
| `IsMobile3` | body | `boolean` | no | Whether Phone 3 is a mobile number. |
| `LastName` | body | `string` | no | Customer last name. |
| `Notes` | body | `string` | no | Additional customer notes. |
| `Phone1` | body | `string` | no | Primary customer phone number. |
| `Phone2` | body | `string` | no | Secondary customer phone number. |
| `Phone3` | body | `string` | no | Third customer phone number. |
| `Postcode` | body | `string` | no | Customer postcode. |
| `ReferralSource` | body | `string` | no | How the customer found the business. |
| `State` | body | `string` | no | Customer state. |
