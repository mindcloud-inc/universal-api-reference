# Find Client IDs by Platform ID with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/find_client_id_by_platform_id`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Find Client IDs by Platform ID](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform_ids[]` | body | `array<string>` | yes | Messenger platform IDs to resolve. |
| `group_id` | body | `number` | yes | Connected channel group ID. |
