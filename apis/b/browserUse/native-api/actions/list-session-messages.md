# List Session Messages with Browser Use

Retrieves session messages from Browser Use.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/:session_id/messages`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [List Session Messages](https://docs.browser-use.com/cloud/api-v3/sessions/list-session-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Return messages after this message ID. |
| `before` | query | `string` | no | Return messages before this message ID. |
| `limit` | query | `number` | no | Maximum number of messages to return, maximum 100. |
| `session_id` | path | `string` | yes | Browser Use session ID. |
