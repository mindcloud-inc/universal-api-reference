# v0: Send Message

Sends a message to an existing v0 chat.

```
POST https://connect.mindcloud.co/v1/universal/v0/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/v0/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The ID of the chat that should receive the message. |
| `message` | string | yes | The prompt or instruction to send to the chat. |
| `system` | string | no |  |
| `attachments[]` | array<object> | no |  |
| `modelConfiguration` | object | no |  |
| `thinking` | boolean | no |  |
| `imageGenerations` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `responseMode` | string | no |  |
| `mcpServerIds[]` | array<string> | no |  |
| `modelId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "authorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "demo": "string",
      "favorite": true,
      "files": [
        {}
      ],
      "id": "string",
      "latestVersion": {
        "demoUrl": "https://example.com",
        "id": "string",
        "status": "string"
      },
      "messages": [
        {}
      ],
      "metadata": {},
      "modelConfiguration": {
        "imageGenerations": true,
        "modelId": "string",
        "thinking": true
      },
      "name": "Ava Chen",
      "object": "string",
      "permissions": {
        "write": true
      },
      "privacy": "string",
      "projectId": "string",
      "shareable": true,
      "text": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `authorId` | string |  |
| `createdAt` | date |  |
| `demo` | string |  |
| `favorite` | boolean |  |
| `files` | array<object> |  |
| `id` | string |  |
| `latestVersion.demoUrl` | string |  |
| `latestVersion.id` | string |  |
| `latestVersion.status` | string |  |
| `messages` | array<object> |  |
| `metadata` | object |  |
| `modelConfiguration.imageGenerations` | boolean |  |
| `modelConfiguration.modelId` | string |  |
| `modelConfiguration.thinking` | boolean |  |
| `name` | string |  |
| `object` | string |  |
| `permissions.write` | boolean |  |
| `privacy` | string |  |
| `projectId` | string |  |
| `shareable` | boolean |  |
| `text` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `POST /v1/chats/:chatId/messages` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.

