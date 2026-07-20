# Delete Survey Export with SmartSurvey

Deletes an existing survey export from SmartSurvey.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/surveys/{surveyId}/exports/{surveyExportId}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Delete Survey Export](https://docs.smartsurvey.io/reference/delete_surveys-surveyid-exports-surveyexportid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
| `surveyExportId` | path | `number` | yes | The id of the export you want to delete |
