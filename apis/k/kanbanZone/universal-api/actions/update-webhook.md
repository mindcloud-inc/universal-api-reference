# Kanban Zone: Update Webhook

Updates an existing webhook in Kanban Zone.

```
PUT https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kanban Zone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kanbanZone/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the webhook to update |
| `board` | string | no | Board public ID |
| `url` | string | no | A valid webhook destination URL |
| `events[]` | array<string> | no | Webhook event names to subscribe to |
| `description` | string | no | Webhook description |
| `enabled` | boolean | no | Whether the webhook is enabled |

## Response

```json
{
  "success": true,
  "data": [
    {
      "board": "string",
      "description": "string",
      "enabled": true,
      "events": [
        "string"
      ],
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `board` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Kanban Zone API, this operation is `PUT /webhooks/:id` (base URL `https://integrations.kanbanzone.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

