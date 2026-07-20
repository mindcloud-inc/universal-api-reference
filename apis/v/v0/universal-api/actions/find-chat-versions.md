# v0: Find Chat Versions

Finds versions for a v0 chat.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-chat-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-chat-versions?connectionId=$CONNECTION_ID&chatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-chat-versions?${params}`, {
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
| `chatId` | string | yes | The ID of the chat whose versions to list. |
| `limit` | number | no | Specifies the maximum number of version records to return in a single response. |
| `cursor` | string | no | Base64 encoded cursor containing pagination data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "demoUrl": "https://example.com",
      "id": "string",
      "object": "string",
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
| `id` | string |  |
| `object` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/chats/:chatId/versions` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-chat-versions.md) for the provider-specific parameters and requirements.

