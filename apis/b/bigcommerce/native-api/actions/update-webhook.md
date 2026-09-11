# Update Webhook with BigCommerce

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/hooks/:webhookId`
- **Base URL:** `https://api.bigcommerce.com/stores/{storeHash}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination` | body | `string` | no | — |
| `webhookId` | path | `string` | no | — |
| `scope` | body | `string` | no | — |
| `events_history_enabled` | body | `boolean` | no | Format: `toggle`. |
| `is_active` | body | `boolean` | no | Format: `toggle`. |
