# Clockify: Create Webhook

Creates a new webhook in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "triggerSourceType": "string",
  "triggerSource[]": [
    "string"
  ],
  "webhookEvent": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "triggerSourceType": "string",
    "triggerSource[]": ["string"],
    "webhookEvent": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `triggerSourceType` | string | yes |  |
| `triggerSource[]` | array<string> | yes |  |
| `webhookEvent` | string | yes |  |
| `url` | string | yes |  |
| `name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authToken": "string",
      "deliveryEnabled": true,
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "triggerSource": [
        "string"
      ],
      "triggerSourceType": "string",
      "url": "https://example.com",
      "userId": "string",
      "webhookEvent": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authToken` | string |  |
| `deliveryEnabled` | boolean |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `triggerSource` | array<string> |  |
| `triggerSourceType` | string |  |
| `url` | string |  |
| `userId` | string |  |
| `webhookEvent` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/webhooks` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

