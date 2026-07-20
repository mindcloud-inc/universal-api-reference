# Hookdeck: Get Issue

Retrieves an issue from Hookdeck.

```
GET https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hookdeck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-issue?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hookdeck/latest/actions/get-issue?${params}`, {
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
| `id` | string | yes | Hookdeck issue ID from the `id` path parameter. |

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

Through the native Hookdeck API, this operation is `GET /issues/:id` (base URL `https://api.hookdeck.com/2025-07-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue.md) for the provider-specific parameters and requirements.

