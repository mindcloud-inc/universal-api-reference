# Save Shipping Label with DateX (Legacy)

## Endpoint

- **Method:** `POST`
- **Path:** `packsize/save_shipping_label`
- **Base URL:** `https://{environment}.wavelength.host/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `containers[]` | body | `array` | no |
| `containers[].order_id` | body | `number` | no |
| `containers[].shipment_id` | body | `string` | no |
| `containers[].shipping_container` | body | `string` | no |
| `containers[].ship_label_zpl` | body | `string` | no |
