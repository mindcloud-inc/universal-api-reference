# Get tasks from a tag with Asana

Retrieves tasks from a tag in Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tags/:tag_gid/tasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get tasks from a tag](https://developers.asana.com/reference/gettasksfortag)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tag_gid` | path | `string` | yes |
