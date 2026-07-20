# Get Order with Handwrite

Retrieves an order from Handwrite.

## Endpoint

- **Method:** `GET`
- **Path:** `/order/:orderId`
- **Base URL:** `https://api.handwrite.io/v1`
- **Official documentation:** [Get Order](https://documentation.handwrite.io/#get-an-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderId` | path | `string` | yes | The Handwrite order ID returned by the send endpoint or visible in the Handwrite app. |
