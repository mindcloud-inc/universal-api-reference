# Get Answer with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/questions/:questionId/answers/:answerId`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Answer](https://www.questionpro.com/api/get-answer.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The QuestionPro survey ID. |
| `questionId` | path | `number` | yes | The QuestionPro question ID. |
| `answerId` | path | `number` | yes | The QuestionPro answer ID. |
