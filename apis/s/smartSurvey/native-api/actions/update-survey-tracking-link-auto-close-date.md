# Update Survey Tracking Link Auto Close Date with SmartSurvey

Updates a survey tracking link auto-close date in SmartSurvey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/links/{id}/autoclosedate`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Update Survey Tracking Link Auto Close Date](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-autoclosedate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are updating |
| `id` | path | `number` | yes | The tracking link id that you are updating the auto close date for |
| `value` | query | `number` | no | The timestamp that you want to use for the new auto close date expressed as Unix Timestamp e.g. seconds from 01-01-1970. If it is not passed, the auto close is disabled. |
