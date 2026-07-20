# List Business Units for User with HubSpot

Retrieves business units for a HubSpot user.

## Endpoint

- **Method:** `GET`
- **Path:** `business-units/v3/business-units/user/:userId`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [List Business Units for User](https://developers.hubspot.com/docs/api-reference/business-units-business-units-v3/business-unit/get-business-units-v3-business-units-user-userId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | The HubSpot user ID. |
| `name[]` | query | `array<string>` | no | A list of business unit names to filter by. |
| `properties[]` | query | `array<string>` | no | Optional business unit properties to include. |
