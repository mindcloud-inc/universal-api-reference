# Update Survey Scheduled Start Date with BlockSurvey

Updates a survey scheduled start date in BlockSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/survey/scheduled_start_date`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Update Survey Scheduled Start Date](https://documents.blocksurvey.io/survey/update-a-survey-scheduled-start-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | The ID of the survey. |
| `scheduledStartDateFlag` | body | `boolean` | yes | Flag to set the scheduled start date. |
| `scheduledStartDate` | body | `number` | yes | The scheduled start date in timestamp format. |
| `teamId` | body | `string` | yes | The team ID. |
