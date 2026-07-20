# Userback: Get Feedback Comment

Retrieves a Userback feedback comment by ID.

```
GET https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-feedback-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-feedback-comment?connectionId=$CONNECTION_ID&feedbackCommentId=4276227" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedbackCommentId": "4276227"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/get-feedback-comment?${params}`, {
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
| `feedbackCommentId` | number | yes | Feedback comment ID to retrieve. Example: `4276227`. |

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

Through the native Userback API, this operation is `GET /feedback/comment/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback-comment.md) for the provider-specific parameters and requirements.

