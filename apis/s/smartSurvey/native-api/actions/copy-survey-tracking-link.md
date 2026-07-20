# Copy Survey Tracking Link with SmartSurvey

Copies an existing survey tracking link in SmartSurvey.

## Endpoint

- **Method:** `PUT`
- **Path:** `/surveys/{surveyId}/links/{id}/copy`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Copy Survey Tracking Link](https://docs.smartsurvey.io/reference/put_surveys-surveyid-links-id-copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are copying |
| `id` | path | `number` | yes | The tracking link id that you are copying from |
| `title` | body | `string` | no | An optional title for the collector |
| `type` | body | `number` | no | The type of collector to create |
