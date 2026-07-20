# Kit: Update Broadcast

Updates an existing broadcast in Kit.

```
PUT https://connect.mindcloud.co/v1/universal/kit/latest/actions/update-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kit/latest/actions/update-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "subject": "string",
  "preview_text": "string",
  "content": "string",
  "description": "string",
  "public": true,
  "published_at": "2026-05-07T12:00:00.000Z",
  "send_at": "2026-05-07T12:00:00.000Z",
  "thumbnail_url": "https://example.com",
  "thumbnail_alt": "string",
  "email_template_id": 1,
  "email_address": "ava@example.com",
  "subscriber_filter[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/update-broadcast', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "subject": "string",
    "preview_text": "string",
    "content": "string",
    "description": "string",
    "public": true,
    "published_at": "2026-05-07T12:00:00.000Z",
    "send_at": "2026-05-07T12:00:00.000Z",
    "thumbnail_url": "https://example.com",
    "thumbnail_alt": "string",
    "email_template_id": 1,
    "email_address": "ava@example.com",
    "subscriber_filter[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Broadcast ID. |
| `subject` | string | yes | Email subject line. |
| `preview_text` | string | yes | Email preview text. |
| `content` | string | yes | HTML email content. |
| `description` | string | yes | Broadcast description. |
| `public` | boolean | yes | Publish broadcast to web when true. |
| `published_at` | date | yes | Published timestamp (ISO8601). |
| `send_at` | date | yes | Scheduled send timestamp (ISO8601). |
| `thumbnail_url` | string | yes | Thumbnail image URL. |
| `thumbnail_alt` | string | yes | Thumbnail alt text. |
| `email_template_id` | number | yes | ID of email template to use. |
| `email_address` | string | yes | Sending email address to use. |
| `subscriber_filter[]` | array<object> | yes | Subscriber targeting filter object array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kit API returns.

## Native endpoint

Through the native Kit API, this operation is `PUT /broadcasts/:id` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-broadcast.md) for the provider-specific parameters and requirements.

