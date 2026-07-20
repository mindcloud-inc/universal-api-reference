# Marketing Master IO: List Chatbot Flows

Retrieves chatbot flows from Marketing Master IO.

```
GET https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chatbot-flows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Marketing Master IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chatbot-flows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/marketingMasterIO/latest/actions/list-chatbot-flows?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "messages": [
        {
          "name": "Ava Chen",
          "payload_id": "string"
        }
      ],
      "name": "Ava Chen",
      "page_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `messages[].name` | string |  |
| `messages[].payload_id` | string |  |
| `name` | string |  |
| `page_id` | string |  |

## Native endpoint

Through the native Marketing Master IO API, this operation is `GET /v1/messenger/flows` (base URL `https://api.marketingmaster.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chatbot-flows.md) for the provider-specific parameters and requirements.

