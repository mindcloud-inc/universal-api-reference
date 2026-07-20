# Get Survey Details with SmartSurvey

Retrieves detailed survey information from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/detailed`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Get Survey Details](https://docs.smartsurvey.io/reference/get_surveys-surveyid-detailed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id of the survey to fetch |
| `translation_id` | query | `number` | no | The id of the translation you want the details in or 0 for the default |
