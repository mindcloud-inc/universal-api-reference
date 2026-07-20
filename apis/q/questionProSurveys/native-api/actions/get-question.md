# Get Question with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/questions/:questionId`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Question](https://www.questionpro.com/api/get-question.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questionId` | path | `number` | yes | The QuestionPro question ID. |
| `surveyId` | path | `number` | yes | The QuestionPro survey ID. |
