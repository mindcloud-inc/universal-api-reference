# Search All Data in Workspace with Kite Suite

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspace/search/:query`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Search All Data in Workspace](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | path | `string` | yes | Search query string. |
| `selectedType` | query | `string` | no | Type of data to filter by (task, project, epic). |
| `projects[]` | query | `array` | no | Array of project IDs to filter by. |
| `assignees[]` | query | `array` | no | Array of assignee IDs to filter by. |
| `reporters[]` | query | `array` | no | Array of reporter IDs to filter by. |
| `status` | query | `string` | no | Status to filter by (done, open). |
| `priorities[]` | query | `array` | no | Array of priorities to filter by. |
