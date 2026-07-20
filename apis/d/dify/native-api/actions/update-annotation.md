# Update Annotation with Dify

Updates an existing annotation in Dify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/apps/annotations/:annotation_id`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [Update Annotation](https://docs.dify.ai/api-reference/annotations/update-annotation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `annotation_id` | path | `string` | yes | Annotation ID to update. |
| `question` | body | `string` | yes | Updated annotation question. |
| `answer` | body | `string` | yes | Updated annotation answer. |
