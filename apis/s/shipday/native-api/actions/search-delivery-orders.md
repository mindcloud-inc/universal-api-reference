# Search Delivery Orders with Shipday

Finds delivery orders in Shipday by query filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/query`
- **Base URL:** `https://api.shipday.com`
- **Official documentation:** [Search Delivery Orders](https://docs.shipday.com/reference/delivery-orders-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startTime` | body | `date` | no | Start timestamp for the delivery-order query window. |
| `endTime` | body | `date` | no | End timestamp for the delivery-order query window. |
| `orderStatus` | body | `string` | no | Order-status filter applied to the query. |
| `startCursor` | body | `number` | no | Start cursor for the returned order range. |
| `endCursor` | body | `number` | no | End cursor for the returned order range. |
