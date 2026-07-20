# Create Dataset with ChatBotKit

## Endpoint

- **Method:** `POST`
- **Path:** `/dataset/create`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [Create Dataset](https://chatbotkit.com/manuals/datasets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alias` | body | `string` | no | Alias for the dataset |
| `name` | body | `string` | no | Name of the dataset |
| `description` | body | `string` | no | Description of the dataset |
| `meta` | body | `object` | no | Metadata for the dataset |
| `blueprintId` | body | `string` | no | Blueprint ID for the dataset |
| `store` | body | `string` | no | Store used by the dataset |
| `reranker` | body | `string` | no | Reranker used by the dataset |
| `recordMaxTokens` | body | `number` | no | Maximum tokens per dataset record |
| `searchMinScore` | body | `number` | no | Minimum search score for dataset results |
| `searchMaxRecords` | body | `number` | no | Maximum number of search results |
| `searchMaxTokens` | body | `number` | no | Maximum tokens used during search |
| `matchInstruction` | body | `string` | no | Instruction used when a match is found |
| `mismatchInstruction` | body | `string` | no | Instruction used when no match is found |
| `separators` | body | `string` | no | Separators used by the dataset |
| `visibility` | body | `list` | no | Visibility of the dataset Accepted values: `private`, `protected`, `public`. |
