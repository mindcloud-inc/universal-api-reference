# Send Callback by Platform ID with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/send_callback_by_platform_id`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Send Callback by Platform ID](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform_ids[]` | body | `array<string>` | yes | Messenger platform IDs to target. |
| `callback_text` | body | `string` | yes | Callback text to deliver to matching clients. |
| `group_id` | body | `number` | yes | Connected channel group ID. |
