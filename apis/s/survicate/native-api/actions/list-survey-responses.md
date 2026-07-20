# List Survey Responses with Survicate

Retrieves responses for a specific Survicate survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/:survey_id/responses`
- **Base URL:** `https://data-api.survicate.com/v2`
- **Official documentation:** [List Survey Responses](https://developers.survicate.com/data-export/response/#list-all-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | path | `string` | yes | The unique identifier of the survey containing the responses. |
| `start` | query | `string` | no | Include responses collected before this ISO 8601 timestamp with microseconds. |
| `end` | query | `string` | no | Include responses collected after this ISO 8601 timestamp with microseconds. |
| `attributes[]` | query | `array<string>` | no | Optional respondent attribute names to include in the response. |
| `filters[]` | query | `array<object>` | no | Optional array of Survicate filter objects for narrowing responses. |
