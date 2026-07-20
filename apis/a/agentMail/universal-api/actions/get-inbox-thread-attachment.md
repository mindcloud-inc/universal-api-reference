# Agent Mail: Get Inbox Thread Attachment

Retrieves a thread attachment from a specific AgentMail inbox.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-thread-attachment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-thread-attachment?connectionId=$CONNECTION_ID&attachmentId=string&inboxId=string&threadId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attachmentId": "string",
  "inboxId": "string",
  "threadId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-inbox-thread-attachment?${params}`, {
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
| `attachmentId` | string | yes | The AgentMail attachment ID. |
| `inboxId` | string | yes | The AgentMail inbox ID. |
| `threadId` | string | yes | The AgentMail thread ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment_id": "string",
      "content_disposition": "string",
      "content_id": "string",
      "content_type": "string",
      "download_url": "https://example.com",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "filename": "Ava Chen",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachment_id` | string | ID of the attachment. |
| `content_disposition` | string | Attachment content disposition. |
| `content_id` | string | Attachment content ID. |
| `content_type` | string | Attachment content type. |
| `download_url` | string | URL to download the attachment. |
| `expires_at` | date | Download URL expiration timestamp. |
| `filename` | string | Attachment filename. |
| `size` | number | Attachment size in bytes. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /inboxes/{inbox_id}/threads/{thread_id}/attachments/{attachment_id}` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox-thread-attachment.md) for the provider-specific parameters and requirements.

