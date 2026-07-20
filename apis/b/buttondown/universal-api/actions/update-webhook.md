# Buttondown: Update Webhook

Updates an existing webhook in Buttondown.

```
PUT https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Buttondown `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "event_types[]": [
    "string"
  ],
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buttondown/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "event_types[]": ["string"],
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Webhook ID. |
| `event_types[]` | array<string> | yes | Exact Buttondown webhook event types to subscribe to. |
| `url` | string | yes | Destination URL for webhook POST requests. |
| `status` | list | no | Whether the webhook is enabled or disabled. One of: `disabled`, `enabled`. |
| `description` | string | no | Optional internal description for the webhook. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signing_key` | string | no | Optional HMAC signing key for webhook verification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "eventTypes": [
        "string"
      ],
      "id": "string",
      "signingKey": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date | When the webhook was created in Buttondown. |
| `description` | string | Optional descriptive label stored on the webhook. |
| `eventTypes` | array<string> | Exact Buttondown event types configured for this webhook. |
| `id` | string | Buttondown webhook ID. |
| `signingKey` | string | Webhook signing key when Buttondown returns it. |
| `status` | string | Current webhook status. |
| `url` | string | Destination URL for webhook deliveries. |

## Native endpoint

Through the native Buttondown API, this operation is `PATCH /webhooks/:id` (base URL `https://api.buttondown.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

