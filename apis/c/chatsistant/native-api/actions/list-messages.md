# List Messages with Chatsistant

Retrieves session message records from Chatsistant.

## Endpoint

- **Method:** `GET`
- **Path:** `/session/:uuid/messages`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [List Messages](https://docs.chatsistant.com/api-reference/messages/fetch_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | no | The session UUID. |
