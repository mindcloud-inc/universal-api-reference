# List messages with Pachca

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List messages](https://dev.pachca.com/reference/messages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chat_id` | query | `number` | yes | Pachca chat ID whose messages should be listed. |
