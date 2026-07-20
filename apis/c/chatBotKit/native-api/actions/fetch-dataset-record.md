# Fetch Dataset Record with ChatBotKit

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset/{datasetId}/record/{recordId}/fetch`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Fetch Dataset Record](https://chatbotkit.com/manuals/dataset-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The ID of the dataset |
| `recordId` | path | `string` | yes | The ID of the record to retrieve |
