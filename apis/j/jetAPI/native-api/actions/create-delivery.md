# Create Delivery with JetAPI

Creates a new message delivery in JetAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/delivery`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Create Delivery](https://docs.jetapi.io/#ea49fe72-5621-405c-ba99-8450050a35ff)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | query | `string` | yes | Recipient phone number in international format. |
| `text` | query | `string` | yes | Message text. |
| `sender_name` | query | `string` | no | — |
| `utm_mark` | query | `string` | no | — |
| `callback_url` | query | `string` | no | Status callback URL. |
| `external_id` | query | `string` | no | Client-side idempotency key. |
| `dispatch_routing[]` | query | `array<string>` | no | — |
| `scheduled_at` | query | `date` | no | UTC datetime in YYYY-MM-DD HH:MM:SS. |
| `priority` | query | `string` | no | high, medium, or low. |
| `username` | query | `string` | no | — |
| `reply_to_message_id` | query | `string` | no | — |
| `tdlib_user_id` | query | `string` | no | — |
| `simulate_typing` | query | `boolean` | no | Whether to simulate typing before sending on WhatsApp. |
| `whatsapp_lid` | query | `string` | no | — |
