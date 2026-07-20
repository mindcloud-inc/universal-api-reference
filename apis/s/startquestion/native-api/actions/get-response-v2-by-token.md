# Get Response V2 by Token with Startquestion

Retrieves a survey response from Startquestion by token with the v2 results format.

## Endpoint

- **Method:** `GET`
- **Path:** `/results/single-sheets/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Get Response V2 by Token](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `token` | query | `string` | yes | Respondent token. |
