# Update Session with Livestorm

Updates an existing session in Livestorm.

## Endpoint

- **Method:** `PATCH`
- **Path:** `sessions/:id`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [Update Session](https://developers.livestorm.co/reference/patch_sessions-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `data.attributes.estimated_started_at` | body | `date` | no | — |
| `data.attributes.timezone` | body | `string` | no | — |
| `data.attributes.name` | body | `string` | no | — |
