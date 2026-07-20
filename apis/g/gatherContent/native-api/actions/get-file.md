# Get File with GatherContent

Retrieves a file from GatherContent.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/files/:file_id`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Get File](https://docs.gathercontent.com/reference/getfile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | path | `string` | yes | File ID. |
| `project_id` | path | `string` | yes | Project ID. |
