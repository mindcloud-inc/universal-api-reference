# Update Gift Card with Gift Up

## Endpoint

- **Method:** `PATCH`
- **Path:** `/gift-cards/:code`
- **Base URL:** `https://api.giftup.app`
- **Official documentation:** [Update Gift Card](https://developer.giftup.com/api#update-a-gift-card)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | — |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the gift card. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the gift card. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations to apply to the gift card. |
