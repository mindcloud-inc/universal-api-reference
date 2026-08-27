# Create Payment Link with Acumatica

Creates a Payment Link for an Sales Order

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/:wse/:endpointVersion/SalesOrder/CreateLink`
- **Base URL:** `{uRL}`

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity` | body | `object` | no |
| `entity.OrderNbr.value` | body | `string` | no |
| `entity.OrderType` | body | `object` | no |
| `entity.OrderType.value` | body | `string` | no |
| `entity.OrderNbr` | body | `object` | no |
| `wse` | path | `string` | yes |
| `endpointVersion` | path | `string` | yes |
