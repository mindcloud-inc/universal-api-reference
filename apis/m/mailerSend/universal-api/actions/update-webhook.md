# MailerSend: Update Webhook



```
PUT https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/update-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/update-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "webhookId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailerSend/latest/actions/update-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "webhookId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `webhookId` | string | yes | ID of the webhook to update. |
| `name` | string | no | Updated webhook name. |
| `url` | string | no | Updated destination URL for the webhook. |
| `events[]` | array<string> | no | Updated MailerSend event types for the webhook. |
| `enabled` | boolean | no | Whether the webhook should be active after update. |

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

Through the native MailerSend API, this operation is `PUT /webhooks/:webhook_id` (base URL `https://api.mailersend.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-webhook.md) for the provider-specific parameters and requirements.

