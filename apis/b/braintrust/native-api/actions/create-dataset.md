# Create Dataset with Braintrust

Creates a new dataset in Braintrust.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/dataset`
- **Base URL:** `https://api.braintrust.dev`
- **Official documentation:** [Create Dataset](https://www.braintrust.dev/docs/api-reference/datasets/create-dataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Project id. |
| `name` | body | `string` | yes | Dataset name. |
