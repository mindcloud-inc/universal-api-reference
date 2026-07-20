# Fetch Dataset with Braintrust

Retrieves events from a dataset in Braintrust.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/dataset/:dataset_id/fetch`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Fetch Dataset](https://braintrust.dev/docs/api-reference/datasets/fetch-dataset-get-form.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes | Dataset id. |
