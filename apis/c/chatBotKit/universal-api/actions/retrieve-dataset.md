# ChatBotKit: Retrieve Dataset



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/retrieve-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/retrieve-dataset?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/retrieve-dataset?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `datasetId` | string | yes | The ID of the dataset to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprintId": "string",
      "createdAt": 1,
      "description": "string",
      "id": "string",
      "matchInstruction": "string",
      "mismatchInstruction": "string",
      "name": "Ava Chen",
      "recordMaxTokens": 1,
      "reranker": "string",
      "searchMaxRecords": 1,
      "searchMaxTokens": 1,
      "searchMinScore": 1,
      "separators": "string",
      "store": "string",
      "updatedAt": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprintId` | string |  |
| `createdAt` | number |  |
| `description` | string |  |
| `id` | string |  |
| `matchInstruction` | string |  |
| `mismatchInstruction` | string |  |
| `name` | string |  |
| `recordMaxTokens` | number |  |
| `reranker` | string |  |
| `searchMaxRecords` | number |  |
| `searchMaxTokens` | number |  |
| `searchMinScore` | number |  |
| `separators` | string |  |
| `store` | string |  |
| `updatedAt` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /dataset/{datasetId}/fetch` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-dataset.md) for the provider-specific parameters and requirements.

