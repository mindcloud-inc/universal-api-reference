# Create Dataset Version From File with PromptLayer Run Agent

Creates a dataset version in PromptLayer from a file.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/public/v2/dataset-versions/from-file`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Create Dataset Version From File](https://docs.promptlayer.com/reference/create-dataset-version-from-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset_group_id` | body | `number` | yes | ID of the dataset group to add a new dataset version to. |
| `file_name` | body | `string` | yes | Name of the uploaded file. |
| `file_content_base64` | body | `string` | yes | Base64-encoded file contents for the dataset version. |
