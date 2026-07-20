# Create Question Choice with MetaSurvey

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/survey/:surveyId/question/:questionId/choice`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey that owns the question. |
| `questionId` | path | `string` | yes | Question that should receive the new choice. |
| `position` | body | `number` | yes | Choice position within the question. |
