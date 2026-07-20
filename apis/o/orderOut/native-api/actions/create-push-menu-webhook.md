# Create Push Menu Webhook with OrderOut

Creates a push menu webhook in OrderOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhooks/push_menu`
- **Base URL:** `https://api.orderout.co`
- **Official documentation:** [Create Push Menu Webhook](https://developers.orderout.co/reference/create-push_menu-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorization_header` | body | `string` | no | Optional auth header |
| `delivery_services` | body | `string` | yes | Target delivery services |
| `endpoint` | body | `string` | yes | Webhook URL |
| `method` | body | `string` | yes | Webhook method |
