# Trigger External Event For Botmother Users with Botmother

Triggers an external event in Botmother for users by bm_id.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{eventUrl}`
- **Official documentation:** [Trigger External Event For Botmother Users](https://docs.botmother.com/article/42097#bm_id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `users_bm[]` | body | `array<string>` | yes | Botmother bm_id values to trigger. |
| `data` | body | `object` | yes | Optional JSON payload copied into last_request. |
