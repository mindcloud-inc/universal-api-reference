# MailoPost: Update Message Webhook

Updates an existing message webhook in MailoPost.

```
PUT https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-message-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-message-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/update-message-webhook', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | MailoPost message webhook identifier. |
| `title` | string | no | Webhook title. |
| `url` | string | no | Webhook delivery URL. Example: `https://example.com/webhook`. |
| `kinds[]` | array<string> | no | Message kinds for this webhook. |
| `events[]` | array<string> | no | Webhook events to subscribe to. |
| `status` | string | no | Webhook status. Example: `active`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "id": 1,
      "kinds": [
        "string"
      ],
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | string |  |
| `id` | number |  |
| `kinds[]` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `PATCH /email/messages_webhooks/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message-webhook.md) for the provider-specific parameters and requirements.

