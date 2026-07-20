# Add Managed User with KleverKey

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/organizations/:organizationId/users/managed`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Add Managed User](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `number` | yes |
| `firstName` | body | `string` | yes |
| `lastName` | body | `string` | yes |
| `deviceSmartCardId` | body | `number` | yes |
| `deviceSmartCardName` | body | `string` | yes |
