# Reach360: Unenroll Group From Learning Path

Removes a group from a Reach360 learning path.

```
DELETE https://connect.mindcloud.co/v1/universal/reach360/latest/actions/unenroll-group-from-learning-path
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/unenroll-group-from-learning-path?connectionId=$CONNECTION_ID&learningPathId=string&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "learningPathId": "string",
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/unenroll-group-from-learning-path?${params}`, {
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
| `learningPathId` | string | yes | The learning path ID. |
| `groupId` | string | yes | The group ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Reach360 API returns.

## Native endpoint

Through the native Reach360 API, this operation is `DELETE /learning-paths/:learningPathId/groups/:groupId` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unenroll-group-from-learning-path.md) for the provider-specific parameters and requirements.

