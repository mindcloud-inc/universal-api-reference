# Add Respondent to Survey with Startquestion

Adds a respondent to a Startquestion survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/respondents/add`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Add Respondent to Survey](https://help.startquestion.com/en/articles/5810169-respondents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | query | `number` | yes | Survey ID. |
| `id_contact` | query | `number` | yes | Contact ID. |
