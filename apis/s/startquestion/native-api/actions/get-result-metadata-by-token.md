# Get Result Metadata by Token with Startquestion

Retrieves survey results metadata from Startquestion by token.

## Endpoint

- **Method:** `GET`
- **Path:** `/results/meta/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Get Result Metadata by Token](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `token` | query | `string` | yes | Respondent token. |
