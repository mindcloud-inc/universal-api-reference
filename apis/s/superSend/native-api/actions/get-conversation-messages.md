# Get Conversation Messages with SuperSend

Retrieves messages from a SuperSend conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/{id}/messages`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Get Conversation Messages](https://docs.supersend.io/docs/conversation)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `limit` | query | `number` | no | Default: 50. Range: 1 to 100. |
| `offset` | query | `number` | no | Default: 0. Range: 0 to inf. |
