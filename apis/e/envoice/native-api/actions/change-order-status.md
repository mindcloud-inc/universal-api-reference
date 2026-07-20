# Change Order Status with Envoice

Updates an order status in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `order/changestatus`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Change Order Status](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `number` | yes | Order identifier. |
| `Reason` | body | `string` | no | Reason for status change. |
| `Status` | body | `string` | yes | New order status. |
