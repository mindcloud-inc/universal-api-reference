# v0: Initialize Chat

Initializes a new chat in v0 from source content.

```
POST https://connect.mindcloud.co/v1/universal/v0/latest/actions/initialize-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/v0/latest/actions/initialize-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/initialize-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no |  |
| `projectId` | string | no |  |
| `name` | string | no |  |
| `chatPrivacy` | string | no |  |
| `metadata` | object | no |  |
| `files[]` | array<object> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `repo` | object | no |  |
| `registry` | object | no |  |
| `zip` | object | no |  |
| `templateId` | string | no |  |

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
| `demo` | string |  |
| `favorite` | boolean |  |
| `files` | array<object> |  |
| `id` | string |  |
| `latestVersion.demoUrl` | string |  |
| `latestVersion.id` | string |  |
| `latestVersion.status` | string |  |
| `messages` | array<object> |  |
| `metadata` | object |  |
| `name` | string |  |
| `object` | string |  |
| `permissions.write` | boolean |  |
| `privacy` | string |  |
| `projectId` | string |  |
| `shareable` | boolean |  |
| `text` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `url` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `POST /v1/chats/init` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initialize-chat.md) for the provider-specific parameters and requirements.

