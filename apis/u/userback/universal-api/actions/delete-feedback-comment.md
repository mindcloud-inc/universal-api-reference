# Userback: Delete Feedback Comment

Deletes a Userback feedback comment.

```
DELETE https://connect.mindcloud.co/v1/universal/userback/latest/actions/delete-feedback-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userback `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/userback/latest/actions/delete-feedback-comment?connectionId=$CONNECTION_ID&feedbackCommentId=4276227" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedbackCommentId": "4276227"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/delete-feedback-comment?${params}`, {
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
| `feedbackCommentId` | number | yes | Feedback comment ID to delete. Example: `4276227`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | boolean |  |

## Native endpoint

Through the native Userback API, this operation is `DELETE /feedback/comment/:id` (base URL `https://rest.userback.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-feedback-comment.md) for the provider-specific parameters and requirements.

