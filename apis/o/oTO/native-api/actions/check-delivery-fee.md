# Check Delivery Fee with OTO

Checks delivery fees in the OTO API.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkDeliveryFee`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Check Delivery Fee](https://help.tryoto.com/en/support/solutions/articles/150000213813-carrier-integrations-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `weight` | body | `string` | yes | Shipment weight used for the fee estimate. |
| `totalDue` | body | `number` | yes | COD or order total due amount. |
| `originCity` | body | `string` | yes | Origin city name. |
| `destinationCity` | body | `string` | yes | Destination city name. |
| `height` | body | `number` | yes | Package height. |
| `width` | body | `number` | yes | Package width. |
| `length` | body | `number` | yes | Package length. |
