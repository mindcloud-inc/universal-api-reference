# Figma: Update Webhook

Updates an existing webhook in Figma.

```
PUT https://connect.mindcloud.co/v1/universal/figma/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/figma/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhook_id": "string",
  "event_type": "string",
  "endpoint": "string",
  "passcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/figma/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhook_id": "string",
    "event_type": "string",
    "endpoint": "string",
    "passcode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhook_id` | string | yes | Webhook identifier to update. |
| `event_type` | list | yes | Webhook event to subscribe to. |
| `endpoint` | string | yes | HTTPS endpoint that receives webhook POST requests. |
| `passcode` | string | yes | Secret string echoed by Figma webhook calls for verification. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list | no | Webhook state after update. |
| `description` | string | no | Optional display name/description for the webhook. |
| `team_id` | string | no | Deprecated legacy team identifier included due OpenAPI required-list inconsistency. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "context": "string",
      "contextId": "string",
      "description": "string",
      "endpoint": "string",
      "eventType": "string",
      "id": "string",
      "passcode": "string",
      "planApiId": "string",
      "status": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string |  |
| `context` | string |  |
| `contextId` | string |  |
| `description` | string |  |
| `endpoint` | string |  |
| `eventType` | string |  |
| `id` | string |  |
| `passcode` | string |  |
| `planApiId` | string |  |
| `status` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Figma API, this operation is `PUT https://api.figma.com/v2/webhooks/:webhook_id` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

