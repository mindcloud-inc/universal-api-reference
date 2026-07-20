# Delete Survey Tracking Link with SmartSurvey

Deletes an existing survey tracking link from SmartSurvey.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/surveys/{surveyId}/links/{id}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Delete Survey Tracking Link](https://docs.smartsurvey.io/reference/delete_surveys-surveyid-links-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose links you are querying |
| `id` | path | `number` | yes | The tracking link id that you want to delete |
