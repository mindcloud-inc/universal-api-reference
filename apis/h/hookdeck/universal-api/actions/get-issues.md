# Hookdeck: Get Issues

Retrieves issues from Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-issues
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-issues?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-issues?${params}`, {
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
      "aggregation_keys": {},
      "auto_resolved_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "dismissed_at": "2026-05-07T12:00:00.000Z",
      "first_seen_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "last_seen_at": "2026-05-07T12:00:00.000Z",
      "last_updated_by": "string",
      "merged_with": "string",
      "opened_at": "2026-05-07T12:00:00.000Z",
      "reference": {},
      "status": "string",
      "team_id": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregation_keys` | object |  |
| `auto_resolved_at` | date |  |
| `created_at` | date |  |
| `data` | object |  |
| `dismissed_at` | date |  |
| `first_seen_at` | date |  |
| `id` | string |  |
| `last_seen_at` | date |  |
| `last_updated_by` | string |  |
| `merged_with` | string |  |
| `opened_at` | date |  |
| `reference` | object |  |
| `status` | string |  |
| `team_id` | string |  |
| `type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Hookdeck API, this operation is `GET /issues` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-issues.md) for the provider-specific parameters and requirements.

