# EDEN AI: List Async Jobs

Retrieves asynchronous jobs from EDEN AI.

```
GET https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-async-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EDEN AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-async-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eDENAI/latest/actions/list-async-jobs?${params}`, {
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
      "items": [
        {}
      ],
      "limit": 1,
      "page": 1,
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
| `items` | array<object> | Async jobs returned by Eden AI. |
| `limit` | number | Page size used for the response. |
| `page` | number | Current page number. |
| `total` | number | Total number of async jobs. |
| `totalPages` | number | Total number of pages. |

## Native endpoint

Through the native EDEN AI API, this operation is `GET /universal-ai/async` (base URL `https://api.edenai.run/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-async-jobs.md) for the provider-specific parameters and requirements.

