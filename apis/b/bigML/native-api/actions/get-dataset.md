# Get Dataset with BigML

Retrieves a dataset from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset/:datasetId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Dataset](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | BigML dataset identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include dataset/. |
