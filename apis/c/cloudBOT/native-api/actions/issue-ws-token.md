# Issue WS Token with Cloud BOT

Issues a WebSocket token in Cloud BOT.

## Endpoint

- **Method:** `POST`
- **Path:** `/:public_id/ws_tokens`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [Issue WS Token](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/post-public_id-ws_tokens)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `public_id` | path | `string` | yes |
| `scopes[]` | body | `array<string>` | yes |
| `keys[]` | body | `array<string>` | yes |
| `expire` | body | `number` | no |
