# Update Survey Tracking Link Text with SmartSurvey

Updates the text of a survey tracking link in SmartSurvey.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/surveys/{surveyId}/links/{id}/linktext`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Update Survey Tracking Link Text](https://docs.smartsurvey.io/reference/patch_surveys-surveyid-links-id-linktext)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are changing |
| `id` | path | `number` | yes | The tracking link id that you are changing the link text for |
| `value` | body | `string` | yes | The new value for the survey link |
