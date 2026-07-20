# Update sale order shipment containers with DateX (Legacy)

Just the markup value, status gets updated automatically

## Endpoint

- **Method:** `POST`
- **Path:** `shipments/shipping_details/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `change.shipment` | body | `object` | no |
| `change.shipment.tracking_number` | body | `string` | no |
| `change.shipping_containers[].id` | body | `number` | no |
| `target` | body | `object` | yes |
| `target.shipment_id` | body | `number` | no |
| `change` | body | `object` | yes |
| `change.shipping_containers[]` | body | `array<object>` | no |
| `change.shipping_containers[].tracking_number` | body | `string` | no |
| `change.shipment.carrier` | body | `string` | no |
| `change.shipping_containers[].length` | body | `number` | no |
| `change.shipment.carrier_service` | body | `string` | no |
| `change.shipping_containers[].width` | body | `number` | no |
| `change.shipping_containers[].height` | body | `number` | no |
| `change.shipping_containers[].dimension_uom` | body | `string` | no |
| `change.shipping_containers[].weight` | body | `number` | no |
| `change.shipping_containers[].weightUom` | body | `string` | no |
| `change.shipping_containers[].carrier` | body | `string` | no |
| `change.shipping_containers[].carrier_service` | body | `string` | no |
