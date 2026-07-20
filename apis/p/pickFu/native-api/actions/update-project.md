# Update Project with PickFu

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/[:id]`
- **Base URL:** `https://api.pickfu.com/v1`
- **Official documentation:** [Update Project](https://www.pickfu.com/docs/api-reference/projects/update-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project GUID. |
| `name` | body | `string` | no | Project name. |
| `description` | body | `string` | no | Project description. |
| `goal` | body | `string` | no | Project goal. |
| `bookmark` | body | `boolean` | no | Set to true to bookmark, false to unbookmark. |
| `archive` | body | `boolean` | no | Set to true to archive, false to unarchive. |
