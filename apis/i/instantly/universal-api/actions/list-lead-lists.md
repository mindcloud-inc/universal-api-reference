# Instantly: List Lead Lists

Retrieves lead lists from Instantly.

```
GET https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-lead-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-lead-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantly/latest/actions/list-lead-lists?${params}`, {
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
      "has_enrichment_task": true,
      "id": "string",
      "name": "Ava Chen",
      "organization_id": "string",
      "owned_by": "string",
      "timestamp_created": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_enrichment_task` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `organization_id` | string |  |
| `owned_by` | string |  |
| `timestamp_created` | date |  |

## Native endpoint

Through the native Instantly API, this operation is `GET /api/v2/lead-lists` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-lead-lists.md) for the provider-specific parameters and requirements.

