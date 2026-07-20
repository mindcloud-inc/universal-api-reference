# Replace Survey Export Emails with SmartSurvey

Replaces email addresses in future scheduled survey exports in SmartSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/surveys/{surveyId}/exports/replace-emails`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Replace Survey Export Emails](https://docs.smartsurvey.io/reference/post_surveys-surveyid-exports-replace-emails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
| `from_email` | body | `string` | yes | The email address to change from (not case-sensitive) |
| `to_email` | body | `string` | yes | The email address to change it to |
