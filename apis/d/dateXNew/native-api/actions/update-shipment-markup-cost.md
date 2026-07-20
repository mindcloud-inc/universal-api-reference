# Update Shipment Markup Cost with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `shipment/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Update Shipment Markup Cost](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipment_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters.order_id` | body | `string` | no | Order ID filter used to find the shipment. |
| `filters.order_lookup` | body | `string` | no | Order lookup filter used to find the shipment. |
| `filters.shipment_id` | body | `string` | no | Shipment ID filter used to find the shipment. |
| `filters.shipment_lookup` | body | `string` | no | Shipment lookup filter used to find the shipment. |
| `update.customer_freight` | body | `number` | yes | New customer freight markup cost. |
