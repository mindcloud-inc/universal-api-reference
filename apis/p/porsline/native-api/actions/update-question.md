# Update Question with Porsline

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/surveys/:survey_id/questions/:id/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Update Question](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1{id}~1/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `id` | path | `number` | yes | Question ID. |
| `title` | body | `string` | no | Question title. |
| `type` | body | `number` | no | Question type. |
| `steps` | body | `number` | no | Number of rating steps. |
| `icon_type` | body | `number` | no | Icon type for rating questions. |
| `answer_required` | body | `boolean` | no | Whether answering the question is required. |
| `duplicate` | query | `string` | no | Whether to duplicate the question during update. |
