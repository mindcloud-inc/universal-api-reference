# Download Latest Survey Export By Type with SmartSurvey

Downloads the latest survey export file by type from SmartSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/exports/latest/download/{reportType}`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [Download Latest Survey Export By Type](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports-latest-download-reporttype)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
| `reportType` | path | `number` | yes | The type of export you want to download |
