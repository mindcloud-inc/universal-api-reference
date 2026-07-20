# List Sessions with Browser Use

Retrieves sessions from Browser Use.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [List Sessions](https://docs.browser-use.com/cloud/api-v3/sessions/list-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number, 1-indexed. |
| `page_size` | query | `number` | no | Number of sessions per page, maximum 100. |
