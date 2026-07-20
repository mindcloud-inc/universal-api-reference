# Close Survey Tracking Link with SmartSurvey

Closes a survey tracking link in SmartSurvey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/links/{id}/close`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Close Survey Tracking Link](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-close)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are closing |
| `id` | path | `number` | yes | The tracking link id that you want to close |
