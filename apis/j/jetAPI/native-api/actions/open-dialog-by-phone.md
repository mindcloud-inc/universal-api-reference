# Open Dialog By Phone with JetAPI

Retrieves a chat dialog link from JetAPI by phone.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/chatter/`
- **Base URL:** `https://api.jetapi.io`
- **Official documentation:** [Open Dialog By Phone](https://docs.jetapi.io/#eef20d97-d724-43b3-b08a-7f0f04884762)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `number` | yes | Unique client ID from the created chat link. |
| `hash` | query | `string` | yes | Unique hash returned by Create Chat Link. |
| `phone` | query | `string` | yes | Recipient phone number. |
| `dispatch_routing` | query | `string` | no | Optional sending channel, whatsapp or tdlib. |
| `sender_id` | query | `number` | no | Optional sender ID for tdlib dialogs. |
| `username` | query | `string` | no | Optional recipient username for tdlib dialogs. |
| `chat_only` | query | `boolean` | no | When true, opens an isolated dialog without chat list navigation. |
