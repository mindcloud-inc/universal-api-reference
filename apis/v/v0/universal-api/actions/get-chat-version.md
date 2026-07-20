# v0: Get Chat Version

Retrieves a chat version from v0 by ID.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-chat-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-chat-version?connectionId=$CONNECTION_ID&chatId=string&versionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string",
  "versionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-chat-version?${params}`, {
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
| `chatId` | string | yes | The ID of the chat that owns the version. |
| `versionId` | string | yes | The ID of the chat version to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "demoUrl": "https://example.com",
      "files": [
        {}
      ],
      "id": "string",
      "object": "string",
      "screenshotUrl": "https://example.com",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `demoUrl` | string |  |
| `files` | array<object> |  |
| `id` | string |  |
| `object` | string |  |
| `screenshotUrl` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/chats/:chatId/versions/:versionId` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat-version.md) for the provider-specific parameters and requirements.

