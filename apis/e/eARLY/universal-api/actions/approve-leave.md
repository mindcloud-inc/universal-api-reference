# EARLY: Approve Leave

Approves a leave in EARLY.

```
PUT https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/approve-leave
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/approve-leave" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "leaveId": "104120"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/approve-leave', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "leaveId": "104120"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `leaveId` | string | yes | Leave ID. Default: `104120`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `POST /api/v4/leaves/:leaveId/approve` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/approve-leave.md) for the provider-specific parameters and requirements.

