# Create Session with Locu

Creates a new work session in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Create Session](https://locu.app/api/docs#tag/sessions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `createdAt` | body | `date` | yes |
| `finishedAt` | body | `date` | yes |
| `id` | body | `string` | no |
