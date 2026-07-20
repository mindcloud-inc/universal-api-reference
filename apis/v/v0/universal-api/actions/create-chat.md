# v0: Create Chat

Creates a new chat in v0.

```
POST https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/create-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | The prompt to send when creating a new chat. |
| `projectId` | string | no | Associates the chat with a specific project in your workspace. |
| `system` | string | no |  |
| `attachments[]` | array<object> | no |  |
| `chatPrivacy` | string | no |  |
| `modelConfiguration` | object | no |  |
| `responseMode` | string | no |  |
| `thinking` | boolean | no |  |
| `imageGenerations` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designSystemId` | string | no |  |
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
      "favorite": true,
      "id": "string",
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
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
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
| `favorite` | boolean |  |
| `id` | string |  |
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
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `POST /v1/chats` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-chat.md) for the provider-specific parameters and requirements.

