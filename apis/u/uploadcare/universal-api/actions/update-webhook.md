# Uploadcare: Update Webhook

Updates an existing webhook in Uploadcare.

```
PUT https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uploadcare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uploadcare/latest/actions/update-webhook', {
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
| `event` | string | no | Updated Uploadcare event type. |
| `id` | number | yes | Uploadcare webhook identifier. |
| `isActive` | boolean | no | Whether the webhook should remain active. |
| `signingSecret` | string | no | Updated shared secret for webhook signature verification. |
| `targetUrl` | string | no | Updated webhook destination URL. |

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

Through the native Uploadcare API, this operation is `PUT /webhooks/:id/` (base URL `https://api.uploadcare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

