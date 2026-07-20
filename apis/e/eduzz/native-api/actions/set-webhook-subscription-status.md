# Set Webhook Subscription Status with Eduzz

Updates the status of a webhook subscription in Eduzz.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/v1/subscription/:id/status`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Set Webhook Subscription Status](https://developers.eduzz.com/reference/api/post-webhook-v1-subscription-id-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Id da inscrição. |
| `status` | body | `string` | no | Status a ser setado. |
