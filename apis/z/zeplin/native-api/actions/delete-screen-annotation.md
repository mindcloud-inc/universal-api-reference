# Delete Screen Annotation with Zeplin

Deletes an existing screen annotation from Zeplin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/screens/{screen_id}/annotations/{annotation_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Delete Screen Annotation](https://docs.zeplin.dev/reference/deletescreenannotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `annotation_id` | path | `string` | yes | Screen annotation id |
