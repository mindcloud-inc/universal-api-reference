# Update Location with ServiceTrade

Updates an existing location in ServiceTrade.

## Endpoint

- **Method:** `PUT`
- **Path:** `location/:locationId`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Update Location](https://api.servicetrade.com/api/docs#resource-location)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationId` | path | `number` | yes | Location to update. |
| `name` | body | `string` | no | Updated name for the location. |
| `phoneNumber` | body | `string` | no | Updated phone number for the location. |
