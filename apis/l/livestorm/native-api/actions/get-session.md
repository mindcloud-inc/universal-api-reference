# Get Session with Livestorm

Retrieves a session from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `sessions/:id`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Get Session](https://developers.livestorm.co/reference/get_sessions-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `include` | query | `string` | no | Include Related Data Send multiple values as a string separated by `,`. |
