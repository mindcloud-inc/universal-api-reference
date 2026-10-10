# Update Contact with PestPac

## Endpoint

- **Method:** `PUT`
- **Path:** `Contacts/:contactId`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`
- **Official documentation:** [Update Contact](https://developer.workwave.com/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `number` | yes |
| `EnteredDate` | body | `date` | no |
| `LastName` | body | `string` | yes |
| `FirstName` | body | `string` | yes |
| `Address` | body | `string` | no |
| `Address2` | body | `string` | no |
| `City` | body | `string` | no |
| `State` | body | `string` | no |
| `Zip` | body | `string` | no |
| `Phone` | body | `string` | no |
| `Fax` | body | `string` | no |
| `MobilePhone` | body | `string` | no |
| `EMail` | body | `string` | no |
| `Comment` | body | `string` | no |
| `LocationID` | body | `number` | yes |
