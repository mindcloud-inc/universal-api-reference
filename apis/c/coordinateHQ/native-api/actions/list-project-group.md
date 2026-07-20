# List Project Group with CoordinateHQ

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/group`
- **Base URL:** `https://app.coordinatehq.com/api/v1`
- **Official documentation:** [List Project Group](https://app.coordinatehq.com/static/API_Documentation.html#groups)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `last_modified_dt` | query | `string` | no |
| `sort` | query | `list<string>` | no |
