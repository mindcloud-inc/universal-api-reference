# Hookdeck: Get Requests

Retrieves requests from Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-requests?${params}`, {
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
      "cli_events_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "events_count": 1,
      "id": "string",
      "ignored_count": 1,
      "ingested_at": "2026-05-07T12:00:00.000Z",
      "original_event_data_id": "string",
      "rejection_cause": "string",
      "source_id": "string",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cli_events_count` | number |  |
| `created_at` | date |  |
| `data` | object |  |
| `events_count` | number |  |
| `id` | string |  |
| `ignored_count` | number |  |
| `ingested_at` | date |  |
| `original_event_data_id` | string |  |
| `rejection_cause` | string |  |
| `source_id` | string |  |
| `team_id` | string |  |
| `updated_at` | date |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Hookdeck API, this operation is `GET /requests` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-requests.md) for the provider-specific parameters and requirements.

