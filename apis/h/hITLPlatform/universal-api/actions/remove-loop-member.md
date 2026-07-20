# HITL Platform: Remove Loop Member



```
DELETE https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/remove-loop-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/remove-loop-member?connectionId=$CONNECTION_ID&id=string&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/remove-loop-member?${params}`, {
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
| `id` | string | yes | The unique identifier of the loop. |
| `userId` | string | yes | The unique identifier of the loop member to remove. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HITL Platform API returns.

## Native endpoint

Through the native HITL Platform API, this operation is `DELETE /api/loops/:id/members/:userId` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-loop-member.md) for the provider-specific parameters and requirements.

