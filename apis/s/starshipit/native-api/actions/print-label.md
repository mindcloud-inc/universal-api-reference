# Print Label with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/shipment`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Print Label](https://api-docs.starshipit.com/#b6bc3576-a43f-4992-86d8-8fdf57f872f6)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | body | `number` | no |
| `carrier` | body | `string` | no |
| `carrier_service_code` | body | `string` | no |
| `packages[]` | body | `array<object>` | no |
| `reprint` | body | `boolean` | no |
