# Get Dataset Rows with PromptLayer Run Agent

Retrieves rows from a PromptLayer dataset.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/datasets/:datasetId/rows`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Get Dataset Rows](https://docs.promptlayer.com/reference/get-dataset-rows)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `number` | yes | The ID of the dataset to retrieve rows from. |
| `q` | query | `string` | no | Search query for filtering rows by content. |
| `workspace_id` | query | `number` | no | Filter by specific workspace ID. |
