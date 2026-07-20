# Tolq: List Translation Requests

Retrieves translation requests from Tolq.

```
GET https://connect.mindcloud.co/v1/universal/tolq/latest/actions/list-translation-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tolq `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tolq/latest/actions/list-translation-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tolq/latest/actions/list-translation-requests?${params}`, {
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
      "completed_at": "2026-05-07T12:00:00.000Z",
      "context_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "status": "string",
      "total_cost": 1,
      "total_keys": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | date |  |
| `context_url` | string |  |
| `created_at` | date |  |
| `id` | number |  |
| `status` | string |  |
| `total_cost` | number |  |
| `total_keys` | number |  |

## Native endpoint

Through the native Tolq API, this operation is `GET /translations/requests` (base URL `https://api.tolq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-translation-requests.md) for the provider-specific parameters and requirements.

