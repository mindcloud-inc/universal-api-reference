# Timely: Filter Reports

Retrieves filtered reports from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/filter-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/filter-reports?connectionId=$CONNECTION_ID&accountId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/filter-reports?${params}`, {
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
| `accountId` | number | yes | Account ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Start date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `until` | date | no | End date for the report period (ISO 8601 format: YYYY-MM-DD) |
| `userIds` | string | no | Comma-separated list of user IDs to filter by |
| `projectIds` | string | no | Comma-separated list of project IDs to filter by |
| `clientIds` | string | no | Comma-separated list of client IDs to filter by |
| `labelIds` | string | no | Comma-separated list of label IDs to filter by |
| `teamIds` | string | no | Comma-separated list of team IDs to filter by (requires teams feature) |
| `stateIds` | string | no | Comma-separated list of state IDs to filter by |
| `groupBy` | string | no | Comma-separated list of grouping keys: clients, users, labels, days, teams. Default: all groups |
| `scope` | string | no | Result scope: totals (aggregated data) or events (individual entries). Default: totals |
| `billed` | string | no | Filter by billed status |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timely API returns.

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/reports/filter` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/filter-reports.md) for the provider-specific parameters and requirements.

