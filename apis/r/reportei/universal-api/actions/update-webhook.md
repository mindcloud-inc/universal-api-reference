# Reportei: Update Webhook

Updates an existing webhook in Reportei.

```
PUT https://connect.mindcloud.co/v1/universal/reportei/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reportei/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID do webhook. |
| `url` | string | no | URL de callback atualizada. |
| `eventType` | string | no | Tipo de evento atualizado. |
| `projectId` | number | no | ID do projeto. |

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

Through the native Reportei API, this operation is `PUT /webhooks/:id` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

