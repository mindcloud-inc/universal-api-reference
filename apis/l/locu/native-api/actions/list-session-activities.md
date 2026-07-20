# List Session Activities with Locu

Retrieves activities for a specific session from Locu.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions/:id/activities`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [List Session Activities](https://locu.app/api/docs#tag/sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID to list activities for. |
