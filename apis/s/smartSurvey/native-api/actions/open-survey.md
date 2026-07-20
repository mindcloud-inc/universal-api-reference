# Open Survey with SmartSurvey

Opens a survey's default tracking link in SmartSurvey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/open`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Open Survey](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-open)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id of the survey you want to open |
