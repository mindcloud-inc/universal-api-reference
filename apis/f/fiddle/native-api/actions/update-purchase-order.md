# Update Purchase Order with Fiddle

Updates an existing purchase order in Fiddle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/purchase-orders`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [Update Purchase Order](https://fiddle.io/rest/api/v2/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | body | `string` | yes | Purchase order ID |
| `notes` | body | `string` | no | Notes |
