# Avaza: List Schedule Series By IDs

Retrieves schedule series by IDs from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-series-by-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-series-by-ids?connectionId=$CONNECTION_ID&scheduleseriesids=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleseriesids": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-schedule-series-by-ids?${params}`, {
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
| `scheduleseriesids` | list<number> | yes |  |
| `updatedafter` | date | no |  |
| `schedulestartdatefrom` | date | no |  |
| `schedulestartdateto` | date | no |  |
| `scheduleenddatefrom` | date | no |  |
| `scheduleenddateto` | date | no |  |
| `userid` | number | no |  |
| `useremail` | string | no |  |
| `timesheetcategoryid` | number | no |  |
| `timesheetcategoryname` | string | no |  |
| `leavetypeid` | number | no |  |
| `projectid` | number | no |  |
| `companyid` | number | no |  |
| `pagesize` | number | no |  |
| `pagenumber` | number | no |  |
| `sort` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/ScheduleSeries` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedule-series-by-ids.md) for the provider-specific parameters and requirements.

