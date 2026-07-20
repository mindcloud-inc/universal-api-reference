# Update Screen Annotation with Zeplin

Updates an existing screen annotation in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/screens/{screen_id}/annotations/{annotation_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Screen Annotation](https://docs.zeplin.dev/reference/updatescreenannotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `screen_id` | path | `string` | yes | Screen id |
| `annotation_id` | path | `string` | yes | Screen annotation id |
| `content` | body | `string` | yes | Content of the annotation |
| `position` | body | `object` | yes | Position of the annotation with respect to top left corner. Values are normalized in [0, 1] |
| `type` | body | `string` | yes | The unique id of the annotation type |
