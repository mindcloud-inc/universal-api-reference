# MailerSend: Create Webhook



```
POST https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/create-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domainId": "string",
  "name": "Ava Chen",
  "url": "https://example.com",
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domainId": "string",
    "name": "Ava Chen",
    "url": "https://example.com",
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domainId` | string | yes | ID of the MailerSend domain that should emit webhook events. |
| `name` | string | yes | Human-readable name for the webhook. |
| `url` | string | yes | Destination URL that should receive MailerSend webhook calls. |
| `events[]` | array<string> | yes | MailerSend event types that should trigger this webhook. |
| `enabled` | boolean | no | Whether the webhook should be active after creation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "domain": {},
      "editable": true,
      "enabled": true,
      "events": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "secret": "string",
      "updatedAt": "string",
      "url": "https://example.com",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `domain` | object |  |
| `editable` | boolean |  |
| `enabled` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `secret` | string |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `version` | number |  |

## Native endpoint

Through the native MailerSend API, this operation is `POST /webhooks` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook.md) for the provider-specific parameters and requirements.

