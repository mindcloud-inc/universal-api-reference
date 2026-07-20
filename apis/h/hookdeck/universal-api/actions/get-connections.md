# Hookdeck: Get Connections

Retrieves connections from Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-connections?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "destination": {},
      "disabled_at": "2026-05-07T12:00:00.000Z",
      "full_name": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "paused_at": "2026-05-07T12:00:00.000Z",
      "rules": [
        {}
      ],
      "source": {},
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `destination` | object |  |
| `disabled_at` | date |  |
| `full_name` | string |  |
| `id` | string |  |
| `name` | string |  |
| `paused_at` | date |  |
| `rules` | array<object> |  |
| `source` | object |  |
| `team_id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Hookdeck API, this operation is `GET /connections` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-connections.md) for the provider-specific parameters and requirements.

