# Avaza: List Timesheets

Retrieves timesheets from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-timesheets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-timesheets?${params}`, {
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
| `updatedafter` | date | no |  |
| `entrydatefrom` | date | no |  |
| `entrydateto` | date | no |  |
| `userid` | number | no | The UserID of a timesheet user to filter timesheets for. Only api users with certain higher roles can see timesheets across multiple users. |
| `useremail` | string | no |  |
| `categoryname` | string | no |  |
| `timesheetentryapprovalstatuscode` | string | no |  |
| `projectid` | number | no |  |
| `taskid` | number | no |  |
| `isbillable` | boolean | no |  |
| `isinvoiced` | boolean | no |  |
| `istimerrunning` | boolean | no |  |
| `includeinvoicedetails` | boolean | no | Defaults to false. When true, the InvoiceIDFK value will be included in the response. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/Timesheet` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-timesheets.md) for the provider-specific parameters and requirements.

