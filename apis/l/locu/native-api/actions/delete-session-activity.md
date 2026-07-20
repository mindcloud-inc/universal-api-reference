# Delete Session Activity with Locu

Deletes an existing session activity from Locu.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sessions/:id/activities/:activityId`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Delete Session Activity](https://locu.app/api/docs#tag/sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID that owns the activity. |
| `activityId` | path | `string` | yes | Activity ID to delete. |
