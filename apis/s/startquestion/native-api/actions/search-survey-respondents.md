# Search Survey Respondents with Startquestion

Searches respondents in a Startquestion survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/respondents/search/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Search Survey Respondents](https://help.startquestion.com/en/articles/5810169-respondents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `email` | query | `string` | no | Respondent email filter. |
