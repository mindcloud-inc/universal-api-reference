# Get Survey Tracking Link with SmartSurvey

Retrieves a survey tracking link from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/links/{id}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Get Survey Tracking Link](https://docs.smartsurvey.io/reference/get_surveys-surveyid-links-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are querying |
| `id` | path | `number` | yes | The tracking link id that you are querying |
