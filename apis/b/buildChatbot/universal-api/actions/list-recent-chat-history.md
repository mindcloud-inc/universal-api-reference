# BuildChatbot: List Recent Chat History

Retrieves recent chat history from BuildChatbot.

```
GET https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-recent-chat-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-recent-chat-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-recent-chat-history?${params}`, {
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
      "data": [
        {}
      ],
      "links": {},
      "page": 1,
      "perPage": 1,
      "primaryLiveChatIntegration": "string",
      "status": "string",
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Recent chat history rows. |
| `links` | object | Pagination links. |
| `page` | number | Current page. |
| `perPage` | number | Items per page. |
| `primaryLiveChatIntegration` | string | Primary live chat channel. |
| `status` | string | Provider response status. |
| `total` | number | Total result count. |
| `totalPages` | number | Total page count. |

## Native endpoint

Through the native BuildChatbot API, this operation is `GET /bot/chat-history/recent/` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-chat-history.md) for the provider-specific parameters and requirements.

