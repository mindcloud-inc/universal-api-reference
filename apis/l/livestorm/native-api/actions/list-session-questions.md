# List Session Questions with Livestorm

Retrieves questions for a session from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `sessions/:id/questions`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Session Questions](https://developers.livestorm.co/reference/get_sessions-id-questions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `include` | query | `string` | no | Include Related Data Send multiple values as a string separated by `,`. |
