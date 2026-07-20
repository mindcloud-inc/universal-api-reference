# ChatBotKit: Create Dataset



```
POST https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-dataset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/create-dataset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alias` | string | no | Alias for the dataset |
| `name` | string | no | Name of the dataset |
| `description` | string | no | Description of the dataset |
| `meta` | object | no | Metadata for the dataset |
| `blueprintId` | string | no | Blueprint ID for the dataset |
| `store` | string | no | Store used by the dataset |
| `reranker` | string | no | Reranker used by the dataset |
| `recordMaxTokens` | number | no | Maximum tokens per dataset record |
| `searchMinScore` | number | no | Minimum search score for dataset results |
| `searchMaxRecords` | number | no | Maximum number of search results |
| `searchMaxTokens` | number | no | Maximum tokens used during search |
| `matchInstruction` | string | no | Instruction used when a match is found |
| `mismatchInstruction` | string | no | Instruction used when no match is found |
| `separators` | string | no | Separators used by the dataset |
| `visibility` | list | no | Visibility of the dataset One of: `private`, `protected`, `public`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /dataset/create` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dataset.md) for the provider-specific parameters and requirements.

