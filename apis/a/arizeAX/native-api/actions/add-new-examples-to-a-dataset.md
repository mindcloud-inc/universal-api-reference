# Add New Examples To A Dataset with Arize AX

Adds new examples to an existing dataset in Arize AX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/datasets/:dataset_id/examples`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Add New Examples To A Dataset](https://arize.com/docs/api-reference/datasets/add-new-examples-to-a-dataset)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes |
| `examples[]` | body | `array<object>` | yes |
