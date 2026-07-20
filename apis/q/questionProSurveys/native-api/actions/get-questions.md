# Get Questions with QuestionPro Surveys

## Endpoint

- **Method:** `GET`
- **Path:** `surveys/:surveyId/questions`
- **Base URL:** `https://api.questionpro.com/a/api/v2`
- **Official documentation:** [Get Questions](https://www.questionpro.com/api/get-questions.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `languageId` | query | `number` | no | Optional QuestionPro language ID for localized question content. |
| `surveyId` | path | `number` | yes | The QuestionPro survey ID. |
