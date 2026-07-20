# Liveblocks: Get Thread

Retrieves a thread from Liveblocks.

```
GET https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-thread?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/get-thread?${params}`, {
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
| `roomId` | string | no | ID of the room. |
| `threadId` | string | no | ID of the thread. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "createdAt": "string",
      "id": "string",
      "metadata": {},
      "resolved": true,
      "roomId": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `createdAt` | string |  |
| `id` | string |  |
| `metadata` | object |  |
| `resolved` | boolean |  |
| `roomId` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Liveblocks API, this operation is `GET /rooms/:roomId/threads/:threadId` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread.md) for the provider-specific parameters and requirements.

