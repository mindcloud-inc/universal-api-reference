# Uploadcare: Create Webhook

Creates a new webhook in Uploadcare.

```
POST https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "targetUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | Uploadcare event type to subscribe to. |
| `isActive` | boolean | no | Whether the webhook should be active immediately. |
| `signingSecret` | string | no | Optional shared secret for webhook signature verification. |
| `targetUrl` | string | yes | Webhook destination URL. |
| `version` | string | no | Webhook payload version. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": 1,
      "isActive": true,
      "project": 1,
      "signingSecret": "string",
      "targetUrl": "https://example.com",
      "updated": "2026-05-07T12:00:00.000Z",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Webhook creation timestamp. |
| `event` | string | Webhook event name. |
| `id` | number | Webhook identifier. |
| `isActive` | boolean | Whether the webhook subscription is active. |
| `project` | number | Uploadcare project identifier. |
| `signingSecret` | string | Webhook signing secret when configured. |
| `targetUrl` | string | Subscribed target URL. |
| `updated` | date | Webhook update timestamp. |
| `version` | string | Webhook payload version. |

## Native endpoint

Through the native Uploadcare API, this operation is `POST /webhooks/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

