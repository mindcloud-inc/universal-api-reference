# Get Question with Porsline

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/surveys/:survey_id/questions/:id/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Get Question](https://developers.porsline.com/#tag/Questions/paths/~1api~1v2~1surveys~1{survey_id}~1questions~1{id}~1/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `id` | path | `number` | yes | Question ID. |
