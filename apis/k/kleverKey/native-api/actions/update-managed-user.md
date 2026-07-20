# Update Managed User with KleverKey

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/organizations/:organizationId/users/managed/:userId`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Update Managed User](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `number` | yes |
| `userId` | path | `number` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
