# List Survey Questions with Survicate

Retrieves questions from a specific Survicate survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/:survey_id/questions`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [List Survey Questions](https://developers.survicate.com/data-export/survey/#list-questions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `string` | yes | The unique identifier of the survey. |
| `start` | query | `string` | no | The question identifier used for paginated results. |
