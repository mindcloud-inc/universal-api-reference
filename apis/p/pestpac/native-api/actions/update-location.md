# Update Location with PestPac

## Endpoint

- **Method:** `PUT`
- **Path:** `Locations/:locationId`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`
- **Official documentation:** [Update Location](https://developer.workwave.com/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `locationId` | path | `number` | yes |
| `LastName` | body | `string` | yes |
| `FirstName` | body | `string` | yes |
| `Address` | body | `string` | yes |
| `Address2` | body | `string` | no |
| `City` | body | `string` | yes |
| `State` | body | `string` | yes |
| `Zip` | body | `string` | yes |
| `Country` | body | `string` | no |
| `Phone` | body | `string` | yes |
| `MobilePhone` | body | `string` | no |
| `EMail` | body | `string` | yes |
| `Website` | body | `string` | no |
| `Active` | body | `boolean` | no |
| `County` | body | `string` | no |
| `TaxCode` | body | `string` | yes |
| `Comment` | body | `string` | no |
| `EnteredDate` | body | `date` | no |
| `Branch` | body | `string` | yes |
| `Type` | body | `string` | yes |
