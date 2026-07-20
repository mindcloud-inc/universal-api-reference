# Create Session Activity with Locu

Creates a new task activity in a Locu session.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:id/activities`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Create Session Activity](https://locu.app/api/docs#tag/sessions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `taskId` | body | `string` | yes |
| `createdAt` | body | `date` | yes |
| `finishedAt` | body | `date` | yes |
| `id` | body | `string` | no |
