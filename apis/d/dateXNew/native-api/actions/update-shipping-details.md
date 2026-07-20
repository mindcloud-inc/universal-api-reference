# Update Shipping Details with DateX

## Endpoint

- **Method:** `POST`
- **Path:** `shipments/shipping_details/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`
- **Official documentation:** [Update Shipping Details](https://sku-mindcloud-api.wavelength.host/documentation/#/functions/post_api_shipments_shipping_details_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target.shipment_id` | body | `number` | yes | Shipment ID whose shipping details should be updated. |
| `change.shipment.tracking_number` | body | `string` | no | Updated shipment tracking number. |
| `change.shipment.carrier` | body | `string` | no | Updated shipment carrier. |
| `change.shipment.carrier_service` | body | `string` | no | Updated shipment carrier service. |
| `change.shipping_containers[]` | body | `array<object>` | no | Array of shipping container update objects, each including the documented container id and changed fields. |
