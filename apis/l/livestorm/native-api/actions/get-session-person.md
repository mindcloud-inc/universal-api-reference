# Get Session Person with Livestorm

Retrieves a session person from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `sessions/:sessionId/people/:id`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Get Session Person](https://developers.livestorm.co/reference/get_sessions-session-id-people-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | Session ID |
| `id` | path | `string` | yes | People ID |
