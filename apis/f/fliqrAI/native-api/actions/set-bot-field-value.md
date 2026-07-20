# Set Bot Field Value with Fliqr AI

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/bot_fields/:bot_field_id`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Set Bot Field Value](https://docs.fliqr.ai/api-reference/accounts/post-accountsbot-fields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_field_id` | path | `number` | yes | Bot field ID. |
| `value` | body | `string` | yes | Value to set for the bot field. |
