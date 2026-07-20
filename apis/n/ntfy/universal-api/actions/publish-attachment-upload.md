# ntfy: Publish Attachment Upload

Publishes a file attachment to an ntfy topic.

```
POST https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-attachment-upload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ntfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-attachment-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/publish-attachment-upload', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "actions": [
        {}
      ],
      "attachment": {},
      "click": "string",
      "event": "string",
      "expires": 1,
      "id": "string",
      "message": "string",
      "priority": 1,
      "sequence_id": "string",
      "tags": [
        "string"
      ],
      "time": 1,
      "title": "string",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actions` | array<object> | Action buttons attached to the message. |
| `attachment` | object | Attachment metadata when the message includes an attachment. |
| `click` | string | URL opened when the notification is clicked. |
| `event` | string | The ntfy event type for the record. |
| `expires` | number | Unix timestamp when the message expires. |
| `id` | string | The ntfy message identifier. |
| `message` | string | The message body text. |
| `priority` | number | Priority from 1 to 5. |
| `sequence_id` | string | Sequence ID for update or delete semantics. |
| `tags` | array<string> | Tags attached to the message. |
| `time` | number | Unix timestamp when the message was created. |
| `title` | string | The message title. |
| `topic` | string | The ntfy topic associated with the message. |

## Native endpoint

Through the native ntfy API, this operation is `PUT /:topic` (base URL `https://ntfy.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-attachment-upload.md) for the provider-specific parameters and requirements.

