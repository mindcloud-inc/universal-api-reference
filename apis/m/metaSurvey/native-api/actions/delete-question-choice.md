# Delete Question Choice with MetaSurvey

## Endpoint

- **Method:** `DELETE`
- **Path:** `/admin/survey/:surveyId/question/:questionId/choice/:choiceId`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey that owns the question. |
| `questionId` | path | `string` | yes | Question that owns the choice. |
| `choiceId` | path | `string` | yes | Choice to delete. |
