# Get Survey Response with SmartSurvey

Retrieves a survey response from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/responses/{responseId}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Get Survey Response](https://docs.smartsurvey.io/reference/get_surveys-surveyid-responses-responseid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id whose Response you are querying |
| `responseId` | path | `number` | yes | The Response id that you are querying |
| `translation_id` | query | `number` | no | The translation id to load - defaults to English |
| `include_labels` | query | `boolean` | no | Whether to include labels in the response - can increase the size of the payload significantly |
