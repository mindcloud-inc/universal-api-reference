# Delete Respondent with Startquestion

Deletes a respondent from a Startquestion survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/respondents/delete`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Delete Respondent](https://help.startquestion.com/en/articles/5810169-respondents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | query | `number` | yes | Survey ID. |
| `id_respondent` | query | `number` | yes | Respondent ID. |
