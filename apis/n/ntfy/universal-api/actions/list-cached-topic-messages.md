# ntfy: List Cached Topic Messages

Retrieves cached messages from an ntfy topic.

```
GET https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/list-cached-topic-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ntfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/list-cached-topic-messages?connectionId=$CONNECTION_ID&topic=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topic": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ntfy/latest/actions/list-cached-topic-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topic` | string | yes | The ntfy topic to read cached messages from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | string | no | Return cached messages since a timestamp, duration, or message ID. Example: `12h \| 1645970742 \| message-id`. |
| `scheduled` | boolean | no | Include delayed or scheduled messages in the cached message list. |
| `id` | string | no | Only return the exact message ID. |
| `message` | string | no | Only return messages whose body exactly matches the given message. |
| `title` | string | no | Only return messages whose title exactly matches the given title. |
| `priority` | string | no | Only return messages that match any of the given priorities. Accepts multiple values in one string, delimited by `,`. Example: `high,urgent`. |
| `tags` | string | no | Only return messages that contain all listed tags. Accepts multiple values in one string, delimited by `,`. Example: `error,alert`. |

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

Through the native ntfy API, this operation is `GET /:topic/json` (base URL `https://ntfy.sh`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-cached-topic-messages.md) for the provider-specific parameters and requirements.

