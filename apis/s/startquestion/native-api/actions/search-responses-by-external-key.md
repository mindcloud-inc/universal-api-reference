# Search Responses by External Key with Startquestion

Retrieves survey responses from Startquestion by external key.

## Endpoint

- **Method:** `GET`
- **Path:** `/results/single-sheets/:id_survey`
- **Base URL:** `https://www.startquestion.com/api/v2`
- **Official documentation:** [Search Responses by External Key](https://help.startquestion.com/en/articles/5810324-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_survey` | path | `number` | yes | Survey ID. |
| `externalKey` | query | `string` | yes | External key filter. |
