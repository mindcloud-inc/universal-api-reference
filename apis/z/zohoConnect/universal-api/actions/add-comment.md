# Zoho Connect: Add Comment

Creates a new comment in Zoho Connect.

```
POST https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scopeId": "string",
  "streamId": "string",
  "commentContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoConnect/latest/actions/add-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scopeId": "string",
    "streamId": "string",
    "commentContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scopeId` | string | yes | ID of the network where the comment should be added. |
| `streamId` | string | yes | The post to comment on. |
| `parentCommentId` | string | no | Reply to an existing comment by supplying its comment ID. |
| `commentContent` | string | yes | Comment text. Maximum length is 10000 characters and it supports mentions plus rich formatting. |
| `fileIds` | string | no | Comma-separated file IDs from the upload Files API. Up to 10 files can be attached. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addComment": {
        "comment": {
          "canDelete": true,
          "canEdit": true,
          "canPinComment": true,
          "canTranslate": true,
          "commentType": "string",
          "content": "string",
          "formatedTime": "string",
          "id": "string",
          "isApproved": true,
          "streamId": "string",
          "streamType": "string",
          "time": "string",
          "url": "https://example.com",
          "userDetails": {
            "bgColor": "string",
            "canFollow": true,
            "id": "string",
            "imageUrl": "https://example.com",
            "name": "Ava Chen",
            "type": "string",
            "zuid": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addComment.comment.canDelete` | boolean |  |
| `addComment.comment.canEdit` | boolean |  |
| `addComment.comment.canPinComment` | boolean |  |
| `addComment.comment.canTranslate` | boolean |  |
| `addComment.comment.commentType` | string |  |
| `addComment.comment.content` | string |  |
| `addComment.comment.formatedTime` | string |  |
| `addComment.comment.id` | string |  |
| `addComment.comment.isApproved` | boolean |  |
| `addComment.comment.streamId` | string |  |
| `addComment.comment.streamType` | string |  |
| `addComment.comment.time` | string |  |
| `addComment.comment.url` | string |  |
| `addComment.comment.userDetails.bgColor` | string |  |
| `addComment.comment.userDetails.canFollow` | boolean |  |
| `addComment.comment.userDetails.id` | string |  |
| `addComment.comment.userDetails.imageUrl` | string |  |
| `addComment.comment.userDetails.name` | string |  |
| `addComment.comment.userDetails.type` | string |  |
| `addComment.comment.userDetails.zuid` | string |  |

## Native endpoint

Through the native Zoho Connect API, this operation is `POST /pulse/api/v2/addComment` (base URL `https://connect.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-comment.md) for the provider-specific parameters and requirements.

