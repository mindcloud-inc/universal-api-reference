# List Clip Projects with Restream

Retrieves clip projects from Restream.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/clips/projects`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [List Clip Projects](https://developers.restream.io/clips/clips-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Cursor from the previous response. |
| `limit` | query | `number` | no | Maximum number of projects to return. |
| `sortBy` | query | `string` | no | Sort order for results: CreatedAt or LastActivity. |
