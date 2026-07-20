# Get Survey Cut Off Date with BlockSurvey

Retrieves a survey cut off date from BlockSurvey.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/survey/cut_off_date`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Get Survey Cut Off Date](https://documents.blocksurvey.io/survey/get-a-survey-cut-off-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | query | `string` | yes | The ID of the survey. |
| `teamId` | query | `string` | no | The team ID. |
