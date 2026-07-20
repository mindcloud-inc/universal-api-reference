# Send Broadcast with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/broadcast`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Send Broadcast](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clients[]` | body | `array<number>` | no | Target Salebot client IDs. |
| `platform_ids[]` | body | `array<string>` | no | Target platform IDs when sending via a specific connected channel. |
| `group_id` | body | `number` | no | Connected channel group ID used with platform_ids. |
| `list` | body | `number` | no | Salebot list identifier to broadcast to. |
| `message_id` | body | `number` | no | Bot block ID to broadcast instead of raw text. |
| `message` | body | `string` | no | Broadcast message text. |
