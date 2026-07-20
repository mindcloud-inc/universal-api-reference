# Kit: Create Broadcast

Creates a new broadcast in Kit.

```
POST https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subject": "string",
  "preview_text": "string",
  "content": "string",
  "description": "string",
  "public": true,
  "published_at": "2026-05-07T12:00:00.000Z",
  "subscriber_filter[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kit/latest/actions/create-broadcast', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subject": "string",
    "preview_text": "string",
    "content": "string",
    "description": "string",
    "public": true,
    "published_at": "2026-05-07T12:00:00.000Z",
    "subscriber_filter[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subject` | string | yes | Email subject line. |
| `preview_text` | string | yes | Email preview text. |
| `content` | string | yes | HTML email content. |
| `description` | string | yes | Broadcast description. |
| `public` | boolean | yes | Publish broadcast to web when true. |
| `published_at` | date | yes | Published timestamp (ISO8601). |
| `subscriber_filter[]` | array<object> | yes | Subscriber targeting filter object array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email_template_id` | number | no | ID of email template to use. |
| `email_address` | string | no | Sending email address to use. |
| `send_at` | date | no | Scheduled send timestamp (ISO8601). |
| `thumbnail_url` | string | no | Thumbnail image URL. |
| `thumbnail_alt` | string | no | Thumbnail alt text. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kit API returns.

## Native endpoint

Through the native Kit API, this operation is `POST /broadcasts` (base URL `https://api.kit.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-broadcast.md) for the provider-specific parameters and requirements.

