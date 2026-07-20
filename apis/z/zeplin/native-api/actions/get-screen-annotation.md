# Get Screen Annotation with Zeplin

Retrieves a screen annotation from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/screens/{screen_id}/annotations/{annotation_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Screen Annotation](https://docs.zeplin.dev/reference/getscreenannotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `annotation_id` | path | `string` | yes | Screen annotation id |
