# Query Dataset Content with Galileo

Finds content in a Galileo dataset by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/datasets/:dataset_id/content/query`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Query Dataset Content](https://docs.galileo.ai/api-reference/datasets/query-dataset-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes | Galileo dataset UUID. |
