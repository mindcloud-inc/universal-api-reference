# Update Dataset Name with Leadboxer

Updates an existing dataset name in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/datasets/{{datasetId}}/name`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Update Dataset Name](https://developers.leadboxer.com/reference/updatedatasetname)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `humanName` | query | `string` | yes | The new dataset name. |
| `datasetId` | path | `string` | yes | The dataset ID. |
| `email` | query | `string` | yes | The user email address. |
