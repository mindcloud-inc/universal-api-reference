# Delete Multiple Messages with Chatsistant

Deletes multiple messages from Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/delete`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Delete Multiple Messages](https://docs.chatsistant.com/api-reference/messages/delete_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | List of message UUIDs to delete. |
