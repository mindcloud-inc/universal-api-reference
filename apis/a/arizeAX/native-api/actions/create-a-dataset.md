# Create a Dataset with Arize AX

Creates a new dataset in Arize AX.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/datasets`
- **Base URL:** `https://api.arize.com`
- **Official documentation:** [Create a Dataset](https://arize.com/docs/api-reference/datasets/create-a-dataset)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `examples[]` | body | `array<object>` | yes |
| `name` | body | `string` | yes |
