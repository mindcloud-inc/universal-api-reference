# Get Sale Order with Evoliz

Retrieves a sale order from Evoliz.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/sale-orders/:orderid`
- **Base URL:** `https://www.evoliz.io`
- **Official documentation:** [Get Sale Order](https://evoliz.io/documentation#tag/Sale%20order/paths/~1api~1v1~1companies~1%7Bcompanyid%7D~1sale-orders~1%7Borderid%7D/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderid` | path | `number` | yes | The Evoliz sale order ID. |
