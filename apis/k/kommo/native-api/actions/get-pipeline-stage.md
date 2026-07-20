# Get Pipeline Stage with Kommo

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/pipelines/:pipeline_id/statuses/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Get Pipeline Stage](https://developers.kommo.com/reference/get-stage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_id` | path | `number` | yes | The pipeline identifier. |
| `pipeline_id` | path | `string` | no | Required path parameter for Get Pipeline Stage. |
| `id` | path | `number` | yes | The stage identifier. |
