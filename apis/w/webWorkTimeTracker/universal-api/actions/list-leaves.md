# WebWork Time Tracker: List Leaves

Retrieves leaves from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-leaves
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-leaves?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-leaves?${params}`, {
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
| `workspaceId` | number | yes | ID of the workspace. |
| `userId` | number | no | Optional filter by user ID. |
| `policyId` | number | no | Optional filter by leave policy ID. |
| `isPaid` | string | no | Optional filter by paid leave status using yes or no. |
| `dateFrom` | string | no | Optional start date filter in YYYY-MM-DD format. |
| `dateTo` | string | no | Optional end date filter in YYYY-MM-DD format. |
| `status` | string | no | Optional filter by leave request status. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebWork Time Tracker API returns.

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /leaves` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-leaves.md) for the provider-specific parameters and requirements.

