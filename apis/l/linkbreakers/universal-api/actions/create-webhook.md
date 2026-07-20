# Linkbreakers: Create a Webhook

Creates a new webhook in Linkbreakers.

```
POST https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Linkbreakers `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpointUrl": "https://example.com",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkbreakers/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpointUrl": "https://example.com",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpointUrl` | string | yes | The webhook endpoint URL. |
| `linkId` | string | no | Optional link ID filter for webhook notifications. |
| `name` | string | yes | The name of the webhook. |
| `source` | string | no | The source of the webhook. |
| `triggers[]` | array<string> | no | Workflow step kinds that should trigger the webhook. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhook": {
        "createdAt": "string",
        "endpointUrl": "https://example.com",
        "failureCount": "string",
        "id": "string",
        "lastDeliveredAt": "string",
        "lastSentAt": "string",
        "linkId": "https://example.com",
        "name": "Ava Chen",
        "source": "string",
        "status": "string",
        "successCount": "string",
        "triggers": [
          "string"
        ],
        "updatedAt": "string",
        "workspaceId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhook` | object | Created webhook configuration. |
| `webhook.createdAt` | string |  |
| `webhook.endpointUrl` | string |  |
| `webhook.failureCount` | string |  |
| `webhook.id` | string |  |
| `webhook.lastDeliveredAt` | string |  |
| `webhook.lastSentAt` | string |  |
| `webhook.linkId` | string |  |
| `webhook.name` | string |  |
| `webhook.source` | string |  |
| `webhook.status` | string |  |
| `webhook.successCount` | string |  |
| `webhook.triggers` | array<string> |  |
| `webhook.updatedAt` | string |  |
| `webhook.workspaceId` | string |  |

## Native endpoint

Through the native Linkbreakers API, this operation is `POST /v1/webhooks` (base URL `https://api.linkbreakers.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

