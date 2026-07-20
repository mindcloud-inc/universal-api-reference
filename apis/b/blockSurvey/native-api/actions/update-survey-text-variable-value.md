# Update Survey Text Variable Value with BlockSurvey

Updates a survey text variable value in BlockSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/survey/text_variable_value`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Update Survey Text Variable Value](https://documents.blocksurvey.io/survey/update-a-survey-text-variable-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | The ID of the survey. |
| `textVariableFlag` | body | `boolean` | yes | Flag to insert, update, or delete the text variable. |
| `textVariableName` | body | `string` | yes | The name of the text variable. |
| `textVariableValue` | body | `string` | yes | The value of the text variable. |
| `teamId` | body | `string` | yes | The team ID. |
