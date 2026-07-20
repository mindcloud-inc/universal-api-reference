# Update Survey Question with MetaSurvey

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/survey/:surveyId/question/:questionId`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey that owns the question. |
| `questionId` | path | `string` | yes | Question to update. |
| `text` | body | `string` | yes | Updated question text. |
