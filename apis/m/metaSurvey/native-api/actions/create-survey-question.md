# Create Survey Question with MetaSurvey

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/survey/:surveyId/question`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey that should receive the new question. |
| `type` | body | `string` | yes | MetaSurvey question type. |
| `position` | body | `number` | yes | Question position within the survey. |
