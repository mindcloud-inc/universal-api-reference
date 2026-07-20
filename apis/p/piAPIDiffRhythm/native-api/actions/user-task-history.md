# User Task History with PiAPI/DiffRhythm

Retrieves your task history from PiAPI/DiffRhythm.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/open/tasks/histories`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [User Task History](https://piapi.ai/docs/piapi-user-history-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | History page number starting at 1. |
| `page_size` | query | `number` | no | Number of history records to return. PiAPI allows up to 100. |
| `start_time` | query | `number` | no | Optional Unix timestamp in seconds. Only return tasks created after this time. |
| `end_time` | query | `number` | no | Optional Unix timestamp in seconds. Only return tasks created before this time. |
