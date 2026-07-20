# List Survey Exports with SmartSurvey

Retrieves all survey exports for a SmartSurvey survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/surveys/{surveyId}/exports`
- **Base URL:** `https://api.smartsurvey.io/v2`
- **Official documentation:** [List Survey Exports](https://docs.smartsurvey.io/reference/get_surveys-surveyid-exports)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | path | `number` | yes | The id of the survey whose exports you are accessing |
