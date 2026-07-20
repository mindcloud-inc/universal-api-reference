# Trigger External Event For Platform Users with Botmother

Triggers an external event in Botmother for platform users.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{eventUrl}`
- **Official documentation:** [Trigger External Event For Platform Users](https://docs.botmother.com/article/42097#request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `platform` | body | `string` | yes | Target platform: tg, fb, viber, vk, or any. |
| `users[]` | body | `array<string>` | yes | Platform user IDs to trigger. |
| `data` | body | `object` | yes | Optional JSON payload copied into last_request. |
