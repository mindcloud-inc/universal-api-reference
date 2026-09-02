# Create Project Item with Jetbuilt

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:projectId/items`
- **Base URL:** `https://app.jetbuilt.com/api/`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `currency_code` | body | `string` | no |
| `external_notes` | body | `string` | no |
| `manufacturer_name` | body | `string` | no |
| `metadata` | body | `object` | no |
| `notes` | body | `string` | no |
| `price` | body | `number` | no |
| `quantity_per_room` | body | `number` | no |
| `room_name` | body | `string` | no |
| `shipping_cost` | body | `number` | no |
| `shipping_price` | body | `number` | no |
| `short_description` | body | `string` | no |
| `system_name` | body | `string` | no |
| `tax_equipment` | body | `boolean` | no |
| `tax_shipping` | body | `boolean` | no |
| `projectId` | path | `string` | yes |
| `model` | body | `string` | no |
