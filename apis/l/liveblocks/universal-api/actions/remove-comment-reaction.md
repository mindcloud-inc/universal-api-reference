# Liveblocks: Remove Comment Reaction

Deletes a comment reaction from Liveblocks.

```
DELETE https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/remove-comment-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/remove-comment-reaction?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/remove-comment-reaction?${params}`, {
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
| `commentId` | string | no | ID of the comment. |
| `emoji` | string | no |  |
| `removedAt` | string | no |  |
| `roomId` | string | no | ID of the room. |
| `threadId` | string | no | ID of the thread. |
| `userId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the comment reaction removal request succeeded. |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms/:roomId/threads/:threadId/comments/:commentId/remove-reaction` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-comment-reaction.md) for the provider-specific parameters and requirements.

