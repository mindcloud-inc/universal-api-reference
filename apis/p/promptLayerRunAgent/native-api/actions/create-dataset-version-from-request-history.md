# Create Dataset Version From Request History with PromptLayer Run Agent

Creates a dataset version in PromptLayer from request history.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/dataset-versions/from-filter-params`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Dataset Version From Request History](https://docs.promptlayer.com/reference/create-dataset-version-from-filter-params)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_group_id` | body | `number` | yes | ID of the dataset group where the new version will be created. |
| `id` | body | `number` | no | Filter to a single request log by its numeric id. |
| `limit` | body | `number` | no | Maximum number of request logs to include. |
