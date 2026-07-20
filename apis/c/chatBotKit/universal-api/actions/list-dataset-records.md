# ChatBotKit: List Dataset Records



```
GET https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-dataset-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBotKit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-dataset-records?connectionId=$CONNECTION_ID&datasetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBotKit/latest/actions/list-dataset-records?${params}`, {
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
| `datasetId` | string | yes | The ID of the dataset |
| `cursor` | string | no | The cursor to use for pagination |
| `order` | list | no | The order of the paginated items One of: `asc`, `desc`. |
| `take` | number | no | The number of items to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "items": [
        {
          "createdAt": 1,
          "id": "string",
          "source": "string",
          "text": "string",
          "updatedAt": 1
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
| `cursor` | string |  |
| `items[].createdAt` | number |  |
| `items[].id` | string |  |
| `items[].source` | string |  |
| `items[].text` | string |  |
| `items[].updatedAt` | number |  |

## Native endpoint

Through the native ChatBotKit API, this operation is `GET /dataset/{datasetId}/record/list` (base URL `https://api.chatbotkit.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dataset-records.md) for the provider-specific parameters and requirements.

