# Create Dataset Record with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/dataset/{datasetId}/record/create`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Create Dataset Record](https://chatbotkit.com/manuals/dataset-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The ID of the dataset |
| `text` | body | `string` | yes | Text of the dataset record |
| `source` | body | `string` | no | Source of the dataset record |
| `meta` | body | `object` | no | Metadata for the dataset record |
