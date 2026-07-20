# Update Item with Gift Up

## Endpoint

- **Method:** `PATCH`
- **Path:** `/items/:id`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Update Item](https://developer.giftup.com/api#update-an-item)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the item. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the item. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the item. |
