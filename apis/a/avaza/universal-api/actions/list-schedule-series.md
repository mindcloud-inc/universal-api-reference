# Avaza: List Schedule Series

Retrieves schedule series from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-series?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-series?${params}`, {
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
| `schedulestartdatefrom` | date | no | Filter for schedules that start on or after a specific date |
| `schedulestartdateto` | date | no | Filter for schedules that start on or before a specific date |
| `scheduleenddatefrom` | date | no | Filter for schedules that end on or after a specific date |
| `scheduleenddateto` | date | no | Filter for schedules that end on or before a specific date |
| `userid` | number | no | The UserID of a schedule user to filter assignments for. Only api users with Admin role can see all schedules across all users. Users with ScheduleUser role can access their own ScheduleSeries. |
| `useremail` | string | no | The email of the user who has been scheduled |
| `timesheetcategoryid` | number | no | Filter for schedule records linked to a specific timesheeet category |
| `timesheetcategoryname` | string | no | Filter for schedule records with a specific timesheeet category name (exact string match) |
| `leavetypeid` | number | no | Filter to records of a particular leave type |
| `projectid` | number | no | Filter to only include books linked to a specific project |
| `companyid` | number | no | Filter to only include records linked to projects, where that project belongs to a specific customer company |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/ScheduleSeries` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-schedule-series.md) for the provider-specific parameters and requirements.

