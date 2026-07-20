# Webex: Create Webhook

Creates a new webhook in Webex.

```
POST https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud webhook",
  "targetUrl": "https://example.com/webex",
  "resource": "messages",
  "event": "created"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud webhook",
    "targetUrl": "https://example.com/webex",
    "resource": "messages",
    "event": "created"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Webhook display name. Example: `MindCloud webhook`. |
| `targetUrl` | string | yes | HTTPS endpoint that receives webhook events. Example: `https://example.com/webex`. |
| `resource` | string | yes | Webhook resource type. Example: `messages`. |
| `event` | string | yes | Webhook event type. Example: `created`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appId": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "event": "string",
      "filter": "string",
      "id": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "ownedBy": "string",
      "resource": "string",
      "status": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | string | Webex app identifier associated with the webhook. |
| `created` | date | Webhook creation timestamp. |
| `createdBy` | string | Person identifier that created the webhook. |
| `event` | string | Event type the webhook listens to. |
| `filter` | string | Optional event filter expression. |
| `id` | string | Webhook identifier. |
| `name` | string | Webhook display name. |
| `orgId` | string | Organization identifier for the webhook. |
| `ownedBy` | string | Webhook ownership scope. |
| `resource` | string | Resource type the webhook listens to. |
| `status` | string | Webhook status. |
| `targetUrl` | string | HTTPS endpoint that receives webhook notifications. |

## Native endpoint

Through the native Webex API, this operation is `POST /webhooks` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

