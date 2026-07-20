# Get Order with Billit

Retrieves a Billit order by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders/:orderID`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [Get Order](https://docs.billit.be/reference/order_getorders_orderid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderID` | path | `number` | yes | Billit OrderID returned when the invoice or order was created. |
