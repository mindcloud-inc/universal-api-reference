# Get Survey Export with SmartSurvey

Retrieves a survey export from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/exports/{surveyExportId}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Get Survey Export](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-surveyexportid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
| `surveyExportId` | path | `number` | yes | The id of the export to fetch |
