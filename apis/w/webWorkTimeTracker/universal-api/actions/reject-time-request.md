# WebWork Time Tracker: Reject Time Request

Rejects a time request in WebWork Time Tracker.

```
PUT https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/reject-time-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/reject-time-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeRequestId": "string",
  "workspaceId": 1,
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/reject-time-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeRequestId": "string",
    "workspaceId": 1,
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeRequestId` | string | yes | Encrypted time request ID. |
| `workspaceId` | number | yes | Workspace ID. |
| `comment` | string | yes | Comment explaining the rejection reason. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebWork Time Tracker API returns.

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `POST /time-requests/:timeRequestId/reject` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reject-time-request.md) for the provider-specific parameters and requirements.

