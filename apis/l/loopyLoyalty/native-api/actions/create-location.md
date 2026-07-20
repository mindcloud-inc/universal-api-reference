# Create Location with Loopy Loyalty

## Endpoint

- **Method:** `POST`
- **Path:** `/location`
- **Base URL:** `https://api.loopyloyalty.com/v1`
- **Official documentation:** [Create Location](https://developer.loopyloyalty.com/#operation/LoopyLoyalty_createLocation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Location name. |
| `lat` | body | `number` | yes | Latitude. |
| `lon` | body | `number` | yes | Longitude. |
| `address` | body | `string` | no | Human readable address of the location. |
| `alt` | body | `number` | no | Altitude. |
| `addressOnCard` | body | `string` | no | Human readable address, including organization name, for rendering on the card. |
| `message` | body | `string` | no | Message shown on the lock-screen when a customer is in the GPS range. |
| `showAddressOnCard` | body | `boolean` | no | Indicates if the address is shown on the card design. |
