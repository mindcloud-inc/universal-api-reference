# Update Document with PestPac

## Endpoint

- **Method:** `PUT`
- **Path:** `Documents/:documentId`
- **Base URL:** `https://api.workwave.com/pestpac/v1/`
- **Official documentation:** [Update Document](https://developer.workwave.com/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `documentId` | path | `number` | yes |
| `LocationID` | body | `number` | yes |
| `Name` | body | `string` | yes |
| `URL` | body | `string` | no |
| `Date` | body | `date` | yes |
| `Tags` | body | `string` | no |
