# Rocketlane: Delete Comment

Deletes a comment from Rocketlane.

```
DELETE https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/delete-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rocketlane `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/delete-comment?connectionId=$CONNECTION_ID&commentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rocketlane/latest/actions/delete-comment?${params}`, {
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
| `commentId` | number | yes | The ID of the message object |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rocketlane API returns.

## Native endpoint

Through the native Rocketlane API, this operation is `DELETE /1.0/comments/:commentId` (base URL `https://api.rocketlane.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-comment.md) for the provider-specific parameters and requirements.

