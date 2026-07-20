# List Project Tasks with CoordinateHQ

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/task`
- **Base URL:** `https://app.coordinatehq.com/api/v1`
- **Official documentation:** [List Project Tasks](https://app.coordinatehq.com/static/API_Documentation.html#tasks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `last_modified_dt` | query | `string` | no |
| `sort` | query | `list<string>` | no |
