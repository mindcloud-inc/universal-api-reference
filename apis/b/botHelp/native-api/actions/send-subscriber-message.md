# Send Subscriber Message with BotHelp

Sends a message to a subscriber in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscribers/:subscriber_id/messages`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Send Subscriber Message](https://main.bothelp.io/swagger)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.api+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of message objects with content values. |
| `subscriber_id` | path | `string` | yes | BotHelp subscriber ID. |
