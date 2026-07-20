# v0: Update Chat

Updates an existing chat in v0.

```
PUT https://connect.mindcloud.co/v1/universal/v0/latest/actions/update-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/v0/latest/actions/update-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/update-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatId` | string | yes | The ID of the chat to update. |
| `name` | string | no |  |
| `privacy` | string | no |  |
| `metadata` | object | no |  |

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
      "id": "string",
      "latestVersion": {
        "demoUrl": "https://example.com",
        "id": "string",
        "status": "string"
      },
      "metadata": {},
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
| `id` | string |  |
| `latestVersion.demoUrl` | string |  |
| `latestVersion.id` | string |  |
| `latestVersion.status` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `permissions.write` | boolean |  |
| `privacy` | string |  |
| `projectId` | string |  |
| `shareable` | boolean |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `PATCH /v1/chats/:chatId` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-chat.md) for the provider-specific parameters and requirements.

