# Get Bulk Messages with ChatDaddy

Retrieves bulk message records from ChatDaddy.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages/bulk`
- **Base URL:** `https://api.chatdaddy.tech/im`
- **Official documentation:** [Get Bulk Messages](https://chatdaddy.stoplight.io/docs/openapi/0f700d7748ca2-bulk-message-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | query | `array<string>` | yes | Message ids to fetch in bulk. |
