# Search Dataset with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/dataset/{datasetId}/search`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Search Dataset](https://chatbotkit.com/manuals/dataset-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The ID of the dataset to search |
| `search` | body | `string` | yes | Search query for the dataset |
| `filter` | body | `object` | no | Filter object for dataset search |
