# Create Survey Tracking Link with SmartSurvey

Creates a new survey tracking link in SmartSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/surveys/{surveyId}/links`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Create Survey Tracking Link](https://docs.smartsurvey.io/reference/post_surveys-surveyid-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The survey id where you want to insert the new collector |
| `title` | body | `string` | no | An optional title for the collector |
| `type` | body | `number` | no | The type of collector to create |
