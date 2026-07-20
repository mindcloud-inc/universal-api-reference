# Userback: List Feedback Comments

Lists the comments for Userback feedback items.

```
GET https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-feedback-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-feedback-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-feedback-comments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "created": "string",
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

Through the native Userback API, this operation is `GET /feedback/comment` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-feedback-comments.md) for the provider-specific parameters and requirements.

