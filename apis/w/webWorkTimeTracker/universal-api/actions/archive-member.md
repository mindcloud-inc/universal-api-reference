# WebWork Time Tracker: Archive Member

Archives a member in WebWork Time Tracker.

```
DELETE https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/archive-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/archive-member?connectionId=$CONNECTION_ID&memberId=1&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "memberId": "1",
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/archive-member?${params}`, {
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
| `memberId` | number | yes |  |
| `workspaceId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebWork Time Tracker API returns.

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `DELETE /members/:memberId` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/archive-member.md) for the provider-specific parameters and requirements.

