# Get Response V3 by ID with Startquestion

Retrieves a survey response from Startquestion by response ID with the v3 results format.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.startquestion.com/api/v3/results/single-sheets/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Get Response V3 by ID](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `responseId` | query | `number` | yes | Response ID. |
