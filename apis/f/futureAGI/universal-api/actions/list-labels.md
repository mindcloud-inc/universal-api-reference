# FutureAGI: List Labels



```
GET https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FutureAGI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-labels?${params}`, {
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
        {
          "createdAt": "string",
          "id": "string",
          "name": "Ava Chen",
          "type": "string"
        }
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
| `results[].createdAt` | string |  |
| `results[].id` | string |  |
| `results[].name` | string |  |
| `results[].type` | string |  |
| `totalPages` | number |  |

## Native endpoint

Through the native FutureAGI API, this operation is `GET /model-hub/annotations-labels/` (base URL `https://api.futureagi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

