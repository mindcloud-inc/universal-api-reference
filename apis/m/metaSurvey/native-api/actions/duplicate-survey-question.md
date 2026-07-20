# Duplicate Survey Question with MetaSurvey

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/survey/:surveyId/question/:questionId/duplicate`
- **Base URL:** `https://api.getmetasurvey.com/api`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `string` | yes | Survey that owns the question. |
| `questionId` | path | `string` | yes | Question to duplicate. |
