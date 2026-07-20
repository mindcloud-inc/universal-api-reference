# Stream: Search Threads

Finds threads in Stream by filter criteria.

```
GET https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stream `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-threads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stream/latest/actions/search-threads?${params}`, {
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
| `filter` | object | no | Thread query filter object. |
| `limit` | number | no | Maximum number of threads to return. |
| `userId` | string | no | User ID context for the query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "duration": "string",
      "threads": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `duration` | string |  |
| `threads` | array<object> |  |

## Native endpoint

Through the native Stream API, this operation is `POST /threads` (base URL `https://chat.stream-io-api.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-threads.md) for the provider-specific parameters and requirements.

