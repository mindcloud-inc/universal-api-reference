# Create Question with Porsline

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/surveys/:survey_id/questions/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Create Question](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `title` | body | `string` | yes | Question title. |
| `type` | body | `number` | yes | Question type. Use 2 for TextQuestion. |
| `prior_question` | body | `number` | no | Prior question id to place the new question after that question. |
