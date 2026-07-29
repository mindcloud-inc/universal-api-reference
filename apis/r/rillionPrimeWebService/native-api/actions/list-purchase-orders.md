# List Purchase Orders with Rillion Prime Web Service

List purchase orders from the Prime purchase order queue by status.

## Endpoint

- **Method:** `POST`
- **Base URL:** `{baseUrl}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PurchaseOrderStatus` | body | `list<number>` | yes | Purchase order status code to filter by: 0=Created, 1=Ordered, 2=Order confirmed, 3=Delivery notified. Accepted values: `0`, `1`, `2`, `3`. |
