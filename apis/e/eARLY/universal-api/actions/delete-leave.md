# EARLY: Delete Leave

Deletes a leave from EARLY.

```
DELETE https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/delete-leave
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/delete-leave?connectionId=$CONNECTION_ID&leaveId=104122" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leaveId": "104122"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/delete-leave?${params}`, {
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
| `leaveId` | string | yes | Leave ID. Default: `104122`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `DELETE /api/v4/leaves/:leaveId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-leave.md) for the provider-specific parameters and requirements.

