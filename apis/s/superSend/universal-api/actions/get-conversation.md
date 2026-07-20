# SuperSend: Get Conversation

Retrieves a conversation from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "identity": {
        "first_name": "Ava",
        "handle": "string",
        "id": "string",
        "last_name": "Chen",
        "photo": "string",
        "type": "string"
      },
      "is_archived": true,
      "is_unread": true,
      "last_activity_at": "2026-05-07T12:00:00.000Z",
      "last_message": {
        "text": "string",
        "timestamp": "2026-05-07T12:00:00.000Z"
      },
      "messages": [
        {
          "attachments": [
            {
              "cloud_url": "https://example.com",
              "file_path": "string",
              "filename": "Ava Chen",
              "id": "string"
            }
          ],
          "conversation_id": "string",
          "html": "string",
          "id": "string",
          "is_from_self": true,
          "is_read": true,
          "job_id": "string",
          "object": "string",
          "platform_type": "string",
          "sender": {
            "email": "ava@example.com",
            "id": "string"
          },
          "status": "string",
          "subject": "string",
          "text": "string",
          "timestamp": "2026-05-07T12:00:00.000Z"
        }
      ],
      "object": "string",
      "participants": [
        {
          "avatar_url": "https://example.com",
          "display_name": "Ava Chen",
          "id": "string",
          "is_self": true,
          "username": "Ava Chen"
        }
      ],
      "platform_type": "string",
      "team_id": "string",
      "title": "string",
      "unread_count": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | string |  |
| `identity.first_name` | string |  |
| `identity.handle` | string |  |
| `identity.id` | string |  |
| `identity.last_name` | string |  |
| `identity.photo` | string |  |
| `identity.type` | string |  |
| `is_archived` | boolean |  |
| `is_unread` | boolean |  |
| `last_activity_at` | date |  |
| `last_message.text` | string |  |
| `last_message.timestamp` | date |  |
| `messages[].attachments[].cloud_url` | string |  |
| `messages[].attachments[].file_path` | string |  |
| `messages[].attachments[].filename` | string |  |
| `messages[].attachments[].id` | string |  |
| `messages[].conversation_id` | string |  |
| `messages[].html` | string |  |
| `messages[].id` | string |  |
| `messages[].is_from_self` | boolean |  |
| `messages[].is_read` | boolean |  |
| `messages[].job_id` | string |  |
| `messages[].object` | string |  |
| `messages[].platform_type` | string |  |
| `messages[].sender.email` | string |  |
| `messages[].sender.id` | string |  |
| `messages[].status` | string |  |
| `messages[].subject` | string |  |
| `messages[].text` | string |  |
| `messages[].timestamp` | date |  |
| `object` | string |  |
| `participants[].avatar_url` | string |  |
| `participants[].display_name` | string |  |
| `participants[].id` | string |  |
| `participants[].is_self` | boolean |  |
| `participants[].username` | string |  |
| `platform_type` | string |  |
| `team_id` | string |  |
| `title` | string |  |
| `unread_count` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /conversations/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

