# Update Address with Bookvault

Updates an existing address in Bookvault.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Addresses`
- **Base URL:** `https://api.bookvault.app/v3`
- **Official documentation:** [Update Address](https://api.bookvault.app/v3/docs#tag/Orders/operation/Addresses_put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addr` | body | `object` | yes | Updated address payload for the selected Bookvault address. |
| `CommonAddrID` | query | `number` | yes | Bookvault common address ID to update. |
