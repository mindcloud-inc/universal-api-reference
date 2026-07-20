# WebWork Time Tracker: Start Time Tracking

Starts time tracking in WebWork Time Tracker.

```
POST https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/start-time-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/start-time-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/start-time-tracking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | ID of the workspace. |
| `userId` | number | yes | ID of the user to start tracking for. |
| `contractId` | number | no | Optional contract ID for project assignment. |
| `taskId` | number | no | Optional task ID. Can only be provided when contract_id is provided. |
| `activityDescription` | string | no | Optional description of the activity being tracked. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebWork Time Tracker API returns.

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `POST /time-tracking/start` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-time-tracking.md) for the provider-specific parameters and requirements.

