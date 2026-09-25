# Update User with Microsoft Entra

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:userId`
- **Base URL:** `https://graph.microsoft.com/v1.0`
- **Official documentation:** [Update User](https://learn.microsoft.com/en-us/graph/api/user-update?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `displayName` | body | `string` | no |
| `userId` | path | `list<string>` | yes |
| `givenName` | body | `string` | no |
| `surname` | body | `string` | no |
| `jobTitle` | body | `string` | no |
| `department` | body | `string` | no |
| `officeLocation` | body | `string` | no |
| `companyName` | body | `string` | no |
| `city` | body | `string` | no |
| `state` | body | `string` | no |
| `country` | body | `string` | no |
| `streetAddress` | body | `string` | no |
| `postalCode` | body | `string` | no |
| `preferredLanguage` | body | `string` | no |
