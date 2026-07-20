# Download Latest Survey Export with SmartSurvey

Downloads the latest survey export file from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/exports/latest/download`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Download Latest Survey Export](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-latest-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
