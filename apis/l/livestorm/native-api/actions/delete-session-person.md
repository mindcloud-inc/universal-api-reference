# Delete Session Person with Livestorm

Removes a person from a session in Livestorm.

## Endpoint

- **Method:** `DELETE`
- **Path:** `sessions/:id/people/:peopleId`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Delete Session Person](https://developers.livestorm.co/reference/delete_sessions-id-people-people-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `people_id` | path | `string` | yes | People ID |
