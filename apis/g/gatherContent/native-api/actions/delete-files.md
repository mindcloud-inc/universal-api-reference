# Delete Files with GatherContent

Deletes files from a GatherContent project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/files`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Delete Files](https://docs.gathercontent.com/reference/deletefile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_ids` | body | `string` | yes | File IDs to delete. |
| `project_id` | path | `string` | yes | Project ID. |
