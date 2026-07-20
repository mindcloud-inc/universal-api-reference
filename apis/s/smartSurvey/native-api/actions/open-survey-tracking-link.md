# Open Survey Tracking Link with SmartSurvey

Opens a survey tracking link in SmartSurvey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/links/{id}/open`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Open Survey Tracking Link](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-open)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are opening |
| `id` | path | `number` | yes | The tracking link id that you want to open |
