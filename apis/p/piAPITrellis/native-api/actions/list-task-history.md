# List Task History with PiAPI/Trellis

Retrieves your task history from PiAPI/Trellis.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/open/tasks/histories`
- **Base URL:** `https://api.piapi.ai`
- **Official documentation:** [List Task History](https://piapi.ai/docs/piapi-user-history-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | History page number. |
| `page_size` | query | `number` | no | Number of history rows to return. |
| `start_time` | query | `number` | no | Unix timestamp lower bound. |
| `end_time` | query | `number` | no | Unix timestamp upper bound. |
