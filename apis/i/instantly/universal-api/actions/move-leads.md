# Instantly: Move Leads

Moves leads to a campaign or list in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/move-leads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/move-leads" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ids[]": [
    "string"
  ],
  "listId": "string",
  "toListId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/move-leads', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ids[]": ["string"],
    "listId": "string",
    "toListId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids[]` | array<string> | yes | Lead IDs to include when moving leads. |
| `listId` | string | yes | Source list ID to filter leads from. |
| `toListId` | string | yes | Destination list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "entity_id": "string",
      "entity_type": "string",
      "id": "string",
      "progress": 1,
      "status": "string",
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `data` | object |  |
| `entity_id` | string |  |
| `entity_type` | string |  |
| `id` | string |  |
| `progress` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updated_at` | date |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/leads/move` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-leads.md) for the provider-specific parameters and requirements.

