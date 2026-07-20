# Update Session Activity with Locu

Updates an existing session activity in Locu.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sessions/:id/activities/:activityId`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Update Session Activity](https://locu.app/api/docs#tag/sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID that owns the activity. |
| `activityId` | path | `string` | yes | Activity ID to update. |
| `createdAt` | body | `date` | no | New activity start timestamp in ISO 8601 format. |
| `finishedAt` | body | `date` | no | New activity end timestamp in ISO 8601 format. |
