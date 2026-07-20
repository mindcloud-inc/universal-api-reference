# WebWork Time Tracker: Get Tracked Hours Report

Retrieves tracked hours reports from WebWork Time Tracker.

```
GET https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-tracked-hours-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-tracked-hours-report?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/get-tracked-hours-report?${params}`, {
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
| `userId` | number | no | Optional filter by specific user ID. |
| `startDate` | string | no | Optional start date for the report in YYYY-MM-DD format. |
| `endDate` | string | no | Optional end date for the report in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WebWork Time Tracker API returns.

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `GET /reports/tracked-hours` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracked-hours-report.md) for the provider-specific parameters and requirements.

