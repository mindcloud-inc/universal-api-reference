# Get Answers with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/questions/:questionId/answers`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Answers](https://www.questionpro.com/api/get-answers.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questionId` | path | `number` | yes | The QuestionPro question ID. |
| `surveyId` | path | `number` | yes | The QuestionPro survey ID. |
