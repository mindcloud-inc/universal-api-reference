# List Datasets with PromptLayer Run Agent

Retrieves a list of datasets from PromptLayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/public/v2/datasets`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [List Datasets](https://docs.promptlayer.com/reference/list-datasets)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_group_id` | query | `number` | no | Filter by specific dataset group ID. |
| `name` | query | `string` | no | Filter datasets by dataset group name. |
| `status` | query | `string` | no | Filter datasets by status: active, deleted, or all. |
