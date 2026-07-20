# Filestage: Create Review Comment

Creates a review comment in Filestage.

```
POST https://connect.mindcloud.co/v1/universal/filestage/latest/actions/create-review-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/create-review-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reviewId": "string",
  "body": "string",
  "teamOnly": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/create-review-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reviewId": "string",
    "body": "string",
    "teamOnly": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewId` | string | yes | Review Id |
| `body` | string | yes | The body or comment contents. A user can be mentioned by formatting in this manner `[~userId]`. Replace this `userId ` with the userId that was gotten from the `Get Mention Suggestions` API endpoint. |
| `teamOnly` | boolean | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attachmentFileURLs[]` | array<string> | no | This is an array of file urls to be attached when creating a comment for a review. |
| `marker` | object | no | The Marker is an object that describe the position of a user comment on the file |

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

Through the native Filestage API, this operation is `POST /reviews/{reviewId}/comments` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-review-comment.md) for the provider-specific parameters and requirements.

