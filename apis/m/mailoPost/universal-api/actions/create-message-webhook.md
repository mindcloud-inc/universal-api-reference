# MailoPost: Create Message Webhook

Creates a new message webhook in MailoPost.

```
POST https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-message-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-message-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "url": "https://example.com/webhook",
  "kinds[]": [
    "string"
  ],
  "events[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-message-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "url": "https://example.com/webhook",
    "kinds[]": ["string"],
    "events[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Webhook title. |
| `url` | string | yes | Webhook delivery URL. Example: `https://example.com/webhook`. |
| `kinds[]` | array<string> | yes | Message kinds for this webhook. |
| `events[]` | array<string> | yes | Webhook events to subscribe to. |

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

Through the native MailoPost API, this operation is `POST /email/messages_webhooks` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message-webhook.md) for the provider-specific parameters and requirements.

