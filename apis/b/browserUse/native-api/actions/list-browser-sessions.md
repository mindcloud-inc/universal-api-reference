# List Browser Sessions with Browser Use

Retrieves browser sessions from Browser Use.

## Endpoint

- **Method:** `GET`
- **Path:** `/browsers`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [List Browser Sessions](https://docs.browser-use.com/cloud/api-v3/browsers/list-browser-sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterBy` | query | `list` | no | Browser session status filter: active or stopped. Accepted values: `0`, `1`. |
| `pageNumber` | query | `number` | no | Page number, 1-indexed. |
| `pageSize` | query | `number` | no | Number of browser sessions per page, maximum 100. |
