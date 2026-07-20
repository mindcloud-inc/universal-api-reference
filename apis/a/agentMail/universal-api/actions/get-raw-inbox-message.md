# Agent Mail: Get Raw Inbox Message

Retrieves the raw message from a specific AgentMail inbox.

```
GET https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-raw-inbox-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-raw-inbox-message?connectionId=$CONNECTION_ID&inboxId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentMail/latest/actions/get-raw-inbox-message?${params}`, {
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
| `inboxId` | string | yes | The AgentMail inbox ID. |
| `messageId` | string | yes | The AgentMail message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "download_url": "https://example.com",
      "expires_at": "2026-05-07T12:00:00.000Z",
      "message_id": "string",
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `download_url` | string | Presigned URL to download the raw message. |
| `expires_at` | date | Download URL expiration timestamp. |
| `message_id` | string | ID of the message. |
| `size` | number | Raw message size in bytes. |

## Native endpoint

Through the native Agent Mail API, this operation is `GET /inboxes/{inbox_id}/messages/{message_id}/raw` (base URL `https://api.agentmail.to/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-raw-inbox-message.md) for the provider-specific parameters and requirements.

