# ChatBotKit: Search Dataset



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/search-dataset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/search-dataset?connectionId=$CONNECTION_ID&datasetId=string&search=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string",
  "search": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/search-dataset?${params}`, {
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
| `datasetId` | string | yes | The ID of the dataset to search |
| `search` | string | yes | Search query for the dataset |
| `filter` | object | no | Filter object for dataset search |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "records": [
        {
          "id": "string",
          "score": 1,
          "source": "string",
          "text": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `records[].id` | string |  |
| `records[].score` | number |  |
| `records[].source` | string |  |
| `records[].text` | string |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `POST /dataset/{datasetId}/search` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-dataset.md) for the provider-specific parameters and requirements.

