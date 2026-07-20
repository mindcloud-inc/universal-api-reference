# Download Survey Export with SmartSurvey

Downloads a survey export file from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/exports/{reportId}/download`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Download Survey Export](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-reportid-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
| `reportId` | path | `number` | yes | The id of the export you want to download |
