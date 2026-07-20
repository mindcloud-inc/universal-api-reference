# Sunshine Conversations: List Integrations

Retrieves configured integrations from Sunshine Conversations.

```
GET https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-integrations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunshine Conversations `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-integrations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunshineConversations/latest/actions/list-integrations?${params}`, {
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
      "integrations": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `integrations` | array<object> | Integration records. |
| `meta` | object | Pagination metadata. |

## Native endpoint

Through the native Sunshine Conversations API, this operation is `GET /apps/:appId/integrations` (base URL `https://api.smooch.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-integrations.md) for the provider-specific parameters and requirements.

