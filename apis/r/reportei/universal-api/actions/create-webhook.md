# Reportei: Create Webhook

Creates a new webhook in Reportei.

```
POST https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com",
  "eventType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reportei/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com",
    "eventType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL de callback para receber os eventos. |
| `eventType` | string | yes | Tipo de evento a monitorar. |
| `projectId` | number | no | ID do projeto para filtrar eventos. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "webhook": {
        "event_type": "string",
        "id": 1,
        "status": 1,
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `webhook.event_type` | string | Webhook event type |
| `webhook.id` | number | Webhook identifier |
| `webhook.status` | number | Webhook status |
| `webhook.url` | string | Webhook callback URL |

## Native endpoint

Through the native Reportei API, this operation is `POST /webhooks` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

