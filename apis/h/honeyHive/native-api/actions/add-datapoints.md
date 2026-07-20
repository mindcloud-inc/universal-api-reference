# Add Datapoints with HoneyHive

Adds datapoints to a dataset in HoneyHive.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasets/{dataset_id}/datapoints`
- **Base URL:** `https://api.honeyhive.ai`
- **Official documentation:** [Add Datapoints](https://github.com/honeyhiveai/typescript-sdk/blob/main/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes | Dataset ID to add datapoints to. |
| `project` | body | `string` | yes | Project name. |
| `data[]` | body | `array<object>` | yes | Data rows to add as datapoints. |
| `mapping` | body | `object` | yes | Mapping for inputs, ground truth, and history. |
