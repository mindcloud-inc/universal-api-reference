# Update Order Export Status with Billit

Updates a Billit order's export status and internal note.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/orders/:orderID`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [Update Order Export Status](https://docs.billit.be/reference/order_patchorders-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderID` | path | `number` | yes | Billit OrderID to patch. |
| `IsSent` | body | `boolean` | no | Billit export flag described in the docs. |
| `InternalInfo` | body | `string` | no | Optional internal free-text note stored on the Billit order. |
