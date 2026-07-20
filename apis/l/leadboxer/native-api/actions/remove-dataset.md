# Remove Dataset with Leadboxer

Deletes an existing dataset from Leadboxer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/datasets/{{datasetId}}`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Remove Dataset](https://developers.leadboxer.com/reference/removedataset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The dataset ID to remove. |
| `email` | query | `string` | yes | The user email address. |
