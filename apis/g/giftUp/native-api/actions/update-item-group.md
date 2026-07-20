# Update Item Group with Gift Up

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:id`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Update Item Group](https://developer.giftup.com/api#update-an-item-group)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the item group. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the item group. |
