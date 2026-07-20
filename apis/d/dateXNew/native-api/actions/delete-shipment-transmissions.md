# Delete Shipment Transmissions with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `sales_orders/shipments/transmissions/delete`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Delete Shipment Transmissions](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_sales_orders_shipments_transmissions_delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipment_ids[]` | body | `array<number>` | yes | Shipment IDs whose transmissions should be deleted. |
