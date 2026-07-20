# List Workspaces with Subnoto

## Endpoint

- **Method:** `POST`
- **Path:** `/public/workspace/list`
- **Base URL:** `https://app.subnoto.com`
- **Official documentation:** [List Workspaces](https://subnoto.com/documentation/developers/openapi/operations/publicworkspacelist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | The page number to return. Defaults to 1. |
| `limit` | body | `number` | no | The number of workspaces to return per page. Defaults to 50 and cannot exceed 50. |
