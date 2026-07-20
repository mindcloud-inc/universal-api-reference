# Get Survey with Survicate

Retrieves a specific survey from Survicate.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/:survey_id`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [Get Survey](https://developers.survicate.com/data-export/survey/#retrieve-survey-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `string` | yes | The unique identifier of the survey to retrieve. |
