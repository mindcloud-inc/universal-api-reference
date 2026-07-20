# Avaza: List Schedule Assignments

Retrieves schedule assignments from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-assignments?${params}`, {
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
| `updatedafter` | date | no | Limit results to records updated after the specified date |
| `scheduledatefrom` | date | no | Filter for schedule assignement that are on or after a specific date |
| `scheduledateto` | date | no | Filter for schedules that are on or before a specific date |
| `scheduleseriesid` | number | no | Filter to records for a particular Schedule Series |
| `userid` | number | no | The UserID of a schedule user to filter assignments for. Only api users with Admin role can see all schedules across all users. Users with ScheduleUser role can access their own ScheduleSeries. |
| `useremail` | string | no | The email of the user who has been scheduled |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/ScheduleAssignment` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-schedule-assignments.md) for the provider-specific parameters and requirements.

