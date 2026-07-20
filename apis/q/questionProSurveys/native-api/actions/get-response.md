# Get Response with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/responses/:responseId`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Response](https://www.questionpro.com/api/get-response.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `responseId` | path | `number` | yes | The QuestionPro response ID. |
| `surveyId` | path | `number` | yes | The QuestionPro survey ID. |
