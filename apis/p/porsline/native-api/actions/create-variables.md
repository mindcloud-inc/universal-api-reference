# Create Variables with Porsline

## Endpoint

- **Method:** `POST`
- **Path:** `/api/surveys/:survey_id/variables/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Create Variables](https://developers.porsline.com/#tag/Variables/paths/~1api~1surveys~1{survey_id}~1variables~1/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `number` | yes | The id of the target survey. |
| `variables` | body | `list<object>` | yes | List of variable objects. Each item should include name, variableSource, type, and optionally hasResponse. |
