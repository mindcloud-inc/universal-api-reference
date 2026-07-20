# Get Result Metadata by Response ID with Startquestion

Retrieves survey results metadata from Startquestion by response ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/results/meta/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Get Result Metadata by Response ID](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `id_response` | query | `number` | yes | Response ID. |
