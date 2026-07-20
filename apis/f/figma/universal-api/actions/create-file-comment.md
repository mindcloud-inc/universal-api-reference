# Figma: Create File Comment

Creates a new comment in a Figma file.

```
POST https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-file-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Figma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-file-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileKey": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/figma/latest/actions/create-file-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileKey": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileKey` | string | yes | Key of the Figma file. |
| `message` | string | yes | Comment text content. |
| `commentId` | string | no | Parent comment ID to create a reply thread. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientMeta` | object | no | Position metadata for where to place the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientMeta": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "fileKey": "string",
      "id": "string",
      "message": "string",
      "orderId": "string",
      "parentId": "string",
      "reactions": [
        {}
      ],
      "resolvedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientMeta` | object |  |
| `createdAt` | date |  |
| `fileKey` | string |  |
| `id` | string |  |
| `message` | string |  |
| `orderId` | string |  |
| `parentId` | string |  |
| `reactions` | array<object> |  |
| `resolvedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Figma API, this operation is `POST /files/:file_key/comments` (base URL `https://api.figma.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file-comment.md) for the provider-specific parameters and requirements.

