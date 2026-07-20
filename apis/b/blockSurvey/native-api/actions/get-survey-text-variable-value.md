# Get Survey Text Variable Value with BlockSurvey

Retrieves a survey text variable value from BlockSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/survey/text_variable_value`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Get Survey Text Variable Value](https://documents.blocksurvey.io/survey/get-a-survey-text-variable-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | query | `string` | yes | The ID of the survey. |
| `textVariableName` | query | `string` | yes | The name of the text variable. |
| `teamId` | query | `string` | no | The team ID. |
