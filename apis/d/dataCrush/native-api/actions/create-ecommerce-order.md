# Create Ecommerce Order with DataCrush

Creates an ecommerce order in DataCrush.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/v1/order/add`
- **Base URL:** `https://api.datacrush.la`
- **Official documentation:** [Create Ecommerce Order](https://help.datacrush.la/hc/es-419/articles/35072600431501-API-Ecommerce-Pedidos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orders_json` | body | `string` | yes | JSON array of order objects. Each order should include at least one item and the provider fields documented for the endpoint. |
