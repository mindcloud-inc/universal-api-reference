# Get Question Statistics with QuestionPro Surveys

## Endpoint

- **Method:** `POST`
- **Path:** `surveys/:surveyId/questions/:questionId/analytics`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Question Statistics](https://www.questionpro.com/api/get-question-statistics.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questionId` | path | `number` | yes | The QuestionPro question ID. |
| `surveyId` | path | `number` | yes | The QuestionPro survey ID. |
