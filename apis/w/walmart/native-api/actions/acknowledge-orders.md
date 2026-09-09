# Acknowledge Orders with Walmart

Acknowledge an entire order, including all of its order lines.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/orders/:purchaseOrderId/acknowledge`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Acknowledge Orders](https://developer.walmart.com/us-marketplace/reference/acknowledgeorders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | path | `string` | yes | Unique Walmart purchaseOrderId that identifies the purchase order. |
| `isDynamicSandbox` | query | `boolean` | no | — |
