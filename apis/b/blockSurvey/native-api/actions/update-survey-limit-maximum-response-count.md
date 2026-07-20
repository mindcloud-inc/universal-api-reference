# Update Survey Limit Maximum Response Count with BlockSurvey

Updates a survey response limit in BlockSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/survey/limit_maximum_response_count`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Update Survey Limit Maximum Response Count](https://documents.blocksurvey.io/survey/update-a-survey-limit-maximum-response-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | The ID of the survey. |
| `limitMaximumResponseCountFlag` | body | `boolean` | yes | Flag to set the maximum response count. |
| `limitMaximumResponseCount` | body | `number` | yes | The maximum response count. |
| `teamId` | body | `string` | yes | The team ID. |
