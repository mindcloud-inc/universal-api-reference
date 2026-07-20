# Update Shipment with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `shipment/update`
- **Base URL:** `https://{environment}.wavelength.host/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filters` | body | `object` | no |
| `filters.order_lookup` | body | `string` | no |
| `filters.order_id` | body | `number` | no |
| `update` | body | `object` | no |
| `filters.shipment_id` | body | `number` | no |
| `filters.shipment_lookup` | body | `string` | no |
