# Update Order with Framework360

## Endpoint

- **Method:** `POST`
- **Path:** `orders/updateStatus`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [Update Order](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Order ID to update. |
| `status` | body | `string` | yes | New order status. |
| `courier` | body | `string` | no | Courier name. |
| `tracking` | body | `string` | no | Tracking code. |
