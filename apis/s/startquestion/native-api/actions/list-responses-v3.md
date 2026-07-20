# List Responses V3 with Startquestion

Retrieves survey responses from Startquestion with the v3 results format.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.startquestion.com/api/v3/results/single-sheets/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [List Responses V3](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Rows per page. |
