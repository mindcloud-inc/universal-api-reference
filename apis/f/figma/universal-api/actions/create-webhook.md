# Figma: Create Webhook

Creates a new webhook in Figma.

```
POST https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_type": "string",
  "context": "string",
  "context_id": "string",
  "endpoint": "string",
  "passcode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_type": "string",
    "context": "string",
    "context_id": "string",
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
| `event_type` | list | yes | Webhook event to subscribe to. |
| `context` | list | yes | Webhook context: team, project, or file. |
| `context_id` | string | yes | ID of the context the webhook is attached to. |
| `endpoint` | string | yes | HTTPS endpoint that receives webhook POST requests. |
| `passcode` | string | yes | Secret string echoed by Figma webhook calls for verification. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | list | no | Initial webhook state. |
| `description` | string | no | Optional display name/description for the webhook. |
| `team_id` | string | no | Deprecated legacy team identifier; prefer context/context_id. |

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

Through the native Figma API, this operation is `POST https://api.figma.com/v2/webhooks` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

