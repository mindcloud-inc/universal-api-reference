# Ghost: Create Webhook

Creates a new webhook in Ghost.

```
POST https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ghost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhooks[0].event": "string",
  "webhooks[0].targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ghost/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhooks[0].event": "string",
    "webhooks[0].targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhooks[0].event` | string | yes |  |
| `webhooks[0].targetUrl` | string | yes |  |
| `webhooks[0].name` | string | no |  |
| `webhooks[0].secret` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhooks[0].integrationId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": "string",
      "createdAt": "string",
      "event": "string",
      "id": "string",
      "integrationId": "string",
      "lastTriggeredAt": {},
      "lastTriggeredError": {},
      "lastTriggeredStatus": {},
      "name": "Ava Chen",
      "secret": "string",
      "targetUrl": "https://example.com",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | string |  |
| `createdAt` | string |  |
| `event` | string |  |
| `id` | string |  |
| `integrationId` | string |  |
| `lastTriggeredAt` | object |  |
| `lastTriggeredError` | object |  |
| `lastTriggeredStatus` | object |  |
| `name` | string |  |
| `secret` | string |  |
| `targetUrl` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Ghost API, this operation is `POST /webhooks/` (base URL `{{credentials.adminDomain}}/ghost/api/admin`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

