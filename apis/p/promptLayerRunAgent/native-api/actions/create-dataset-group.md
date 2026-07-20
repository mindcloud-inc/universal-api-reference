# Create Dataset Group with PromptLayer Run Agent

Creates a new dataset group in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/dataset-groups`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Dataset Group](https://docs.promptlayer.com/reference/create-dataset-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name for the dataset group. Must be unique within the workspace. |
| `workspace_id` | body | `number` | no | Workspace ID. Defaults to the workspace associated with the API key. |
| `folder_id` | body | `number` | no | Optional folder ID to create the dataset group inside. |
