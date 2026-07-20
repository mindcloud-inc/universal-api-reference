# Update Location with Loopy Loyalty

## Endpoint

- **Method:** `PATCH`
- **Path:** `/location/:id`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Update Location](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_updateLocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Location ID. |
| `name` | body | `string` | no | Location name. |
| `lat` | body | `number` | no | Latitude. |
| `lon` | body | `number` | no | Longitude. |
| `address` | body | `string` | no | Human readable address of the location. |
| `alt` | body | `number` | no | Altitude. |
| `addressOnCard` | body | `string` | no | Human readable address, including organization name, for rendering on the card. |
| `message` | body | `string` | no | Message shown on the lock-screen when a customer is in the GPS range. |
| `showAddressOnCard` | body | `boolean` | no | Indicates if the address is shown on the card design. |
