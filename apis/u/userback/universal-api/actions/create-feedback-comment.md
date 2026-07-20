# Userback: Create Feedback Comment

Creates a comment on a Userback feedback item.

```
POST https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedbackId": "7378423",
  "comment": "Comment added by the Stage 3 build batch."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedbackId": "7378423",
    "comment": "Comment added by the Stage 3 build batch."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedbackId` | number | yes | Parent feedback ID. Example: `7378423`. |
| `comment` | string | yes | Feedback comment text. Example: `Comment added by the Stage 3 build batch.`. |
| `isPublic` | boolean | no | Whether the comment is public. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `replyCommentId` | number | no | Reply target comment ID. Example: `12345`. |
| `userId` | number | no | Comment author user ID. Example: `105101`. |
| `guestEmail` | string | no | Guest commenter email. Example: `guest@example.com`. |
| `guestName` | string | no | Guest commenter name. Example: `Guest User`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "created": "string",
      "feedback": {
        "created": "string",
        "description": "string",
        "dueDate": "string",
        "email": "ava@example.com",
        "feedbackType": "string",
        "id": 1,
        "modified": "string",
        "name": "Ava Chen",
        "projectId": 1,
        "shareKey": "string",
        "title": "string"
      },
      "feedbackId": 1,
      "guestEmail": "ava@example.com",
      "guestName": "Ava Chen",
      "id": 1,
      "isPublic": true,
      "isResolved": true,
      "modified": "string",
      "replyCommentId": 1,
      "screenshotNum": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string |  |
| `created` | string |  |
| `feedback.created` | string |  |
| `feedback.description` | string |  |
| `feedback.dueDate` | string |  |
| `feedback.email` | string |  |
| `feedback.feedbackType` | string |  |
| `feedback.id` | number |  |
| `feedback.modified` | string |  |
| `feedback.name` | string |  |
| `feedback.projectId` | number |  |
| `feedback.shareKey` | string |  |
| `feedback.title` | string |  |
| `feedbackId` | number |  |
| `guestEmail` | string |  |
| `guestName` | string |  |
| `id` | number |  |
| `isPublic` | boolean |  |
| `isResolved` | boolean |  |
| `modified` | string |  |
| `replyCommentId` | number |  |
| `screenshotNum` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native Userback API, this operation is `POST /feedback/comment` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback-comment.md) for the provider-specific parameters and requirements.

