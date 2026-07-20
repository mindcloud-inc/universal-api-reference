# Filestage: Pin or Unpin a Comment

Pins or unpins a comment in Filestage.

```
PUT https://connect.mindcloud.co/v1/universal/filestage/latest/actions/pin-or-unpin-a-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/pin-or-unpin-a-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/pin-or-unpin-a-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentId` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isPinned` | boolean | no | When the value is `true` the comment is pinned and when the value is `false`, the comment is unpinned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        "string"
      ],
      "author": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "id": "string"
      },
      "body": "string",
      "copiedFrom": {
        "copiedTime": "2026-05-07T12:00:00.000Z",
        "copyType": "string",
        "originalCommentId": "string",
        "userId": "string"
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "fileVersionId": "string",
      "id": "string",
      "isPinned": true,
      "isResolved": true,
      "likes": [
        {}
      ],
      "marker": {},
      "mentioned": {
        "displayName": "Ava Chen",
        "email": "ava@example.com",
        "fullName": "Ava Chen",
        "id": "string"
      },
      "replies": [
        {}
      ],
      "reviewId": "string",
      "shareLink": "https://example.com",
      "teamOnly": true,
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<string> |  |
| `author` | object |  |
| `author.displayName` | string |  |
| `author.email` | string |  |
| `author.fullName` | string |  |
| `author.id` | string |  |
| `body` | string |  |
| `copiedFrom` | object |  |
| `copiedFrom.copiedTime` | date |  |
| `copiedFrom.copyType` | string |  |
| `copiedFrom.originalCommentId` | string |  |
| `copiedFrom.userId` | string |  |
| `createdTime` | date |  |
| `fileVersionId` | string |  |
| `id` | string |  |
| `isPinned` | boolean |  |
| `isResolved` | boolean |  |
| `likes` | array<object> |  |
| `marker` | object |  |
| `mentioned` | array<object> |  |
| `mentioned.displayName` | string |  |
| `mentioned.email` | string |  |
| `mentioned.fullName` | string |  |
| `mentioned.id` | string |  |
| `replies` | array<object> |  |
| `reviewId` | string |  |
| `shareLink` | string |  |
| `teamOnly` | boolean |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Filestage API, this operation is `PUT /comments/{commentId}/pinned` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pin-or-unpin-a-comment.md) for the provider-specific parameters and requirements.

