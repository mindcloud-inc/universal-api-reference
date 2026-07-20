# Create Push Order Webhook with OrderOut

Creates a push order webhook in OrderOut.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhooks/push_order`
- **Base URL:** `https://api.orderout.co`
- **Official documentation:** [Create Push Order Webhook](https://developers.orderout.co/reference/create-push_order-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `authorization_header` | body | `string` | no | Optional auth header |
| `endpoint` | body | `string` | yes | Webhook URL |
| `method` | body | `string` | yes | Webhook method |
