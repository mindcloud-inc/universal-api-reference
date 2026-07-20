# List Dataset Records with ChatBotKit

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset/{datasetId}/record/list`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [List Dataset Records](https://chatbotkit.com/manuals/dataset-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetId` | path | `string` | yes | The ID of the dataset |
| `cursor` | query | `string` | no | The cursor to use for pagination |
| `order` | query | `list` | no | The order of the paginated items Accepted values: `asc`, `desc`. |
| `take` | query | `number` | no | The number of items to retrieve |
