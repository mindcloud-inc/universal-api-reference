# Create deal with OkoCRM

Creates a new deal in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Create deal](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `budget` | body | `string` | no | Deal budget. |
| `name` | body | `string` | yes | Deal name. |
| `pipeline_id` | body | `number` | yes | The pipeline to create the deal in. |
| `stages_id` | body | `number` | yes | The starting stage for the new deal. |
