# Letta: List Runs

Retrieves a list of runs from Letta.

```
GET https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Letta `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-runs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letta/latest/actions/list-runs?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completed_at` | date |  |
| `created_at` | date |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Letta API, this operation is `GET /v1/runs/` (base URL `https://api.letta.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-runs.md) for the provider-specific parameters and requirements.

