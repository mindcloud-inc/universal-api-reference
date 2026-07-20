# Close Survey with SmartSurvey

Closes a survey and its tracking links in SmartSurvey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/close`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Close Survey](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-close)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id of the survey you want to close |
