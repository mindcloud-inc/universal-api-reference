# FutureAGI: List Queues



```
GET https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-queues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FutureAGI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-queues?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-queues?${params}`, {
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
      "count": 1,
      "currentPage": 1,
      "next": "string",
      "previous": "string",
      "results": [
        {}
      ],
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `currentPage` | number |  |
| `next` | string |  |
| `previous` | string |  |
| `results` | array<object> |  |
| `totalPages` | number |  |

## Native endpoint

Through the native FutureAGI API, this operation is `GET /model-hub/annotation-queues/` (base URL `https://api.futureagi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-queues.md) for the provider-specific parameters and requirements.

