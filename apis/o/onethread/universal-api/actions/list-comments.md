# Onethread: List Comments



```
GET https://connect.mindcloud.co/v1/universal/onethread/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onethread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onethread/latest/actions/list-comments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onethread/latest/actions/list-comments?${params}`, {
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
      "_id": "string",
      "account": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "mentionLists": [
        {}
      ],
      "taskId": "string",
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `account` | object |  |
| `createdAt` | date |  |
| `mentionLists` | array<object> |  |
| `taskId` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Onethread API, this operation is `GET /comments` (base URL `https://api.onethread.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.

