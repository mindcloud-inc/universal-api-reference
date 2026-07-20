# Instantly: Update Lead List

Updates an existing lead list in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-lead-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-lead-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-lead-list', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Lead list ID. |
| `name` | string | yes | Updated lead list name. |

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

Through the native Instantly API, this operation is `PATCH /api/v2/lead-lists/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lead-list.md) for the provider-specific parameters and requirements.

