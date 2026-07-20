# Send Subscriber Message By CUID with BotHelp

Sends a message to a subscriber by CUID in BotHelp.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/subscribers/cuid/:subscriber_cuid/messages`
- **Base URL:** `https://api.bothelp.io`
- **Official documentation:** [Send Subscriber Message By CUID](https://main.bothelp.io/swagger)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.api+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of message objects with content values. |
| `subscriber_cuid` | path | `string` | yes | BotHelp subscriber CUID. |
