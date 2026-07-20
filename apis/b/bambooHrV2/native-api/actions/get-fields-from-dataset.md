# Get Fields from Dataset with BambooHR

Retrieves fields for a dataset from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/datasets/:datasetName/fields`
- **Base URL:** `https://mindcloud.bamboohr.com/api`
- **Official documentation:** [Get Fields from Dataset](https://documentation.bamboohr.com/reference/get-fields-from-dataset-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetName` | path | `string` | yes | The BambooHR dataset name to inspect. |
