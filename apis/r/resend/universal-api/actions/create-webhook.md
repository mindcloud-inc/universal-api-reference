# Resend: Create Webhook

Creates a new webhook in Resend.

```
POST https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endpoint": "string",
  "events[]": "contact.created"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/resend/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endpoint": "string",
    "events[]": "contact.created"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endpoint` | string | yes | The URL where webhook events will be sent |
| `events[]` | array<string> | yes | Array of event types to subscribe to One of: `contact.created`, `contact.deleted`, `contact.updated`, `domain.created`, `domain.deleted`, `domain.updated`, `email.bounced`, `email.clicked`, `email.complained`, `email.delivered`, `email.delivery_delayed`, `email.failed`, `email.opened`, `email.received`, `email.scheduled`, `email.sent`, `email.suppressed`. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "signingSecret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Webhook identifier. |
| `object` | string | Object type identifier. |
| `signingSecret` | string | Webhook signing secret returned at creation time. |

## Native endpoint

Through the native Resend API, this operation is `POST /webhooks` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

