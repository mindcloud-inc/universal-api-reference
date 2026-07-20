# Update Survey Tracking Link with SmartSurvey

Updates an existing survey tracking link in SmartSurvey.

## Endpoint

- **Method:** `PUT`
- **Path:** `/surveys/{surveyId}/links/{id}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Update Survey Tracking Link](https://docs.smartsurvey.io/reference/put_surveys-surveyid-links-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are updating |
| `id` | path | `number` | yes | The tracking link id that you are updating |
| `title` | body | `string` | no | The title of the tracking link |
