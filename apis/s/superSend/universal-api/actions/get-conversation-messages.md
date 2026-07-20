# SuperSend: Get Conversation Messages

Retrieves messages from a SuperSend conversation.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-conversation-messages?${params}`, {
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
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments[].cloud_url` | string |  |
| `attachments[].file_path` | string |  |
| `attachments[].filename` | string |  |
| `attachments[].id` | string |  |
| `conversation_id` | string |  |
| `html` | string |  |
| `id` | string |  |
| `is_from_self` | boolean |  |
| `is_read` | boolean |  |
| `job_id` | string |  |
| `object` | string |  |
| `platform_type` | string |  |
| `sender.email` | string |  |
| `sender.id` | string |  |
| `status` | string |  |
| `subject` | string |  |
| `text` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /conversations/{id}/messages` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-conversation-messages.md) for the provider-specific parameters and requirements.

