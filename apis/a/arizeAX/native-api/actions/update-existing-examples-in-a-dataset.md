# Update Existing Examples In A Dataset with Arize AX

Updates existing examples in a dataset in Arize AX.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/datasets/:dataset_id/examples`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Update Existing Examples In A Dataset](https://arize.com/docs/api-reference/datasets/update-existing-examples-in-a-dataset)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `dataset_id` | path | `string` | yes |
| `examples[]` | body | `array<object>` | yes |
