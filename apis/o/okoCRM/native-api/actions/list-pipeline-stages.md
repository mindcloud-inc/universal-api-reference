# List pipeline stages with OkoCRM

Retrieves pipeline stages for a pipeline in OkoCRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/pipelines/stages/[:pipeline_id]`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [List pipeline stages](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `number` | yes | The OkoCRM pipeline ID. |
