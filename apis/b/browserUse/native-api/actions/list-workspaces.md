# List Workspaces with Browser Use

Retrieves workspaces from Browser Use.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [List Workspaces](https://docs.browser-use.com/cloud/api-v3/workspaces/list-workspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageNumber` | query | `number` | no | Page number, 1-indexed. |
| `pageSize` | query | `number` | no | Number of workspaces per page, maximum 100. |
