# v0: Get Chat

Retrieves a chat from v0 by ID.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-chat?connectionId=$CONNECTION_ID&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-chat?${params}`, {
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
| `chatId` | string | yes | The ID of the chat to retrieve. |

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

Through the native v0 API, this operation is `GET /v1/chats/:chatId` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

