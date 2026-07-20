# Zoho Cliq: Get Thread Main Message

Retrieves the main message of a Zoho Cliq thread.

```
GET https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/get-thread-main-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Cliq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/get-thread-main-message?connectionId=$CONNECTION_ID&threadChatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "threadChatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCliq/latest/actions/get-thread-main-message?${params}`, {
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
| `threadChatId` | string | yes | The chat ID of the thread whose main message should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "id": "string",
      "is_pinned": true,
      "is_read": true,
      "parent_resource_id": "string",
      "revision": 1,
      "sender": {},
      "thread_information": {},
      "time": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | The message content payload. |
| `id` | string | The parent message identifier. |
| `is_pinned` | boolean | Whether the message is pinned. |
| `is_read` | boolean | Whether the message has been read. |
| `parent_resource_id` | string | The parent channel unique identifier. |
| `revision` | number | The message revision. |
| `sender` | object | The sender details. |
| `thread_information` | object | The thread metadata including the thread chat ID. |
| `time` | number | The message time in milliseconds. |
| `type` | string | The message type. |

## Native endpoint

Through the native Zoho Cliq API, this operation is `GET /threads/:threadChatId/messages/main` (base URL `https://cliq.zoho.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread-main-message.md) for the provider-specific parameters and requirements.

