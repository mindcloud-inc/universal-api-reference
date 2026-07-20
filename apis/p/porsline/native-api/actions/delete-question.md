# Delete Question with Porsline

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/surveys/:survey_id/questions/:id/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Delete Question](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1{id}~1/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `id` | path | `number` | yes | Question ID. |
