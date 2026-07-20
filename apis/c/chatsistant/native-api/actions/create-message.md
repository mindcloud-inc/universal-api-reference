# Create Message with Chatsistant

Creates a new session message in Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/session/:uuid/message/stream`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Create Message](https://docs.chatsistant.com/api-reference/messages/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | The message query. |
| `uuid` | path | `string` | no | The session UUID. |
