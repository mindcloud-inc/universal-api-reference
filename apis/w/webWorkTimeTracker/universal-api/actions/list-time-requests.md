# WebWork Time Tracker: List Time Requests

Retrieves time requests from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-time-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-time-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=1&dateFrom=string&dateTo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "1",
  "dateFrom": "string",
  "dateTo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/list-time-requests?${params}`, {
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
| `workspaceId` | number | yes | Workspace ID. |
| `dateFrom` | string | yes | Start date for filtering time requests. |
| `dateTo` | string | yes | End date for filtering time requests. |
| `status` | string | no | Optional status filter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebWork Time Tracker API returns.

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /time-requests` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-requests.md) for the provider-specific parameters and requirements.

