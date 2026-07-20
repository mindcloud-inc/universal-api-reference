# Update Survey Cut Off Date with BlockSurvey

Updates a survey cut off date in BlockSurvey.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/survey/cut_off_date`
- **Base URL:** `https://api3.blocksurvey.io`
- **Official documentation:** [Update Survey Cut Off Date](https://documents.blocksurvey.io/survey/update-a-survey-cut-off-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | The ID of the survey. |
| `cutOffDateFlag` | body | `boolean` | yes | Flag to set the cut-off date. |
| `cutOffDate` | body | `number` | yes | The cut-off date in timestamp format. |
| `teamId` | body | `string` | yes | The team ID. |
