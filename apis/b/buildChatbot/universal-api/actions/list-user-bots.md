# BuildChatbot: List User Bots

Retrieves user bot records from BuildChatbot.

```
GET https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-user-bots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildChatbot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-user-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildChatbot/latest/actions/list-user-bots?${params}`, {
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
      "page": "string",
      "perPage": 1,
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
| `data` | array<object> | Bots returned for the tenant. |
| `links` | object | Pagination links. |
| `page` | string | Current page. |
| `perPage` | number | Items per page. |
| `status` | string | Provider response status. |
| `total` | number | Total result count. |
| `totalPages` | number | Total page count. |

## Native endpoint

Through the native BuildChatbot API, this operation is `GET /user/get_all_user_bots/` (base URL `https://api.buildchatbot.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-bots.md) for the provider-specific parameters and requirements.

