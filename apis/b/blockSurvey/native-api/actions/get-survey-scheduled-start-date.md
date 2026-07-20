# Get Survey Scheduled Start Date with BlockSurvey

Retrieves a survey scheduled start date from BlockSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/survey/scheduled_start_date`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Get Survey Scheduled Start Date](https://documents.blocksurvey.io/survey/get-a-survey-scheduled-start-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | query | `string` | yes | The ID of the survey. |
| `teamId` | query | `string` | no | The team ID. |
