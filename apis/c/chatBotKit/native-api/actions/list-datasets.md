# List Datasets with ChatBotKit

## Endpoint

- **Method:** `GET`
- **Path:** `/dataset/list`
- **Base URL:** `https://api.chatbotkit.com/v1`
- **Official documentation:** [List Datasets](https://chatbotkit.com/manuals/datasets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | The cursor to use for pagination |
| `order` | query | `list` | no | The order of the paginated items Accepted values: `asc`, `desc`. |
| `take` | query | `number` | no | The number of items to retrieve |
| `meta` | query | `object` | no | Key-value pairs to filter the partner users by metadata |
