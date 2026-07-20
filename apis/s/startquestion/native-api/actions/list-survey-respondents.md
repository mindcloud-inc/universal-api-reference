# List Survey Respondents with Startquestion

Retrieves respondents for a Startquestion survey.

## Endpoint

- **Method:** `GET`
- **Path:** `/respondents/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [List Survey Respondents](https://help.startquestion.com/en/articles/5810169-respondents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
