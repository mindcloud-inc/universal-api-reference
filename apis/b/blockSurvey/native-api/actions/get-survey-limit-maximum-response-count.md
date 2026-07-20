# Get Survey Limit Maximum Response Count with BlockSurvey

Retrieves a survey response limit from BlockSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/survey/limit_maximum_response_count`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Get Survey Limit Maximum Response Count](https://documents.blocksurvey.io/survey/get-a-survey-limit-maximum-response-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | query | `string` | yes | The ID of the survey. |
| `teamId` | query | `string` | no | The team ID. |
