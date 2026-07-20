# Check OTO Delivery Fee with OTO

Checks OTO delivery fees in the OTO API.

## Endpoint

- **Method:** `POST`
- **Path:** `/checkOTODeliveryFee`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [Check OTO Delivery Fee](https://help.tryoto.com/en/support/solutions/articles/150000213820-oto-flex-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originCity` | body | `string` | yes | Origin city name. |
| `destinationCity` | body | `string` | yes | Destination city name. |
| `boxes[0].width` | body | `number` | yes | Width of the first box in the quote request. |
| `boxes[0].length` | body | `number` | yes | Length of the first box in the quote request. |
| `boxes[0].height` | body | `number` | yes | Height of the first box in the quote request. |
| `boxes[0].weight` | body | `number` | yes | Weight of the first box in the quote request. |
| `boxes[0].boxName` | body | `string` | yes | Name of the first box in the quote request. |
