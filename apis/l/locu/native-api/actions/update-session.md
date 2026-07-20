# Update Session with Locu

Updates an existing session in Locu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sessions/:id`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Update Session](https://locu.app/api/docs#tag/sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID to update. |
| `createdAt` | body | `date` | no | New session start timestamp in ISO 8601 format. |
| `finishedAt` | body | `date` | no | New session end timestamp in ISO 8601 format. |
