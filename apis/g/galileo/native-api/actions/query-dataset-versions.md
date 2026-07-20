# Query Dataset Versions with Galileo

Finds versions for a Galileo dataset by query.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/datasets/:dataset_id/versions/query`
- **Base URL:** `https://api.galileo.ai`
- **Official documentation:** [Query Dataset Versions](https://docs.galileo.ai/api-reference/datasets/query-dataset-versions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes | Galileo dataset UUID. |
