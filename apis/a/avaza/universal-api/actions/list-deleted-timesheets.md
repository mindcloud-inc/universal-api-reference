# Avaza: List Deleted Timesheets

Retrieves deleted timesheet entries from Avaza.

```
GET https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-deleted-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-deleted-timesheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avaza/latest/actions/list-deleted-timesheets?${params}`, {
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
| `userid` | number | no | Filter by user ID |
| `deletedafter` | date | no | Filter entries deleted after this UTC date |
| `entrydatefrom` | date | no | Filter by original timesheet entry date (start) |
| `entrydateto` | date | no | Filter by original timesheet entry date (end) |
| `pagesize` | number | no | Number of items per page |
| `pagenumber` | number | no | Page number (starts from 1) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `GET /api/Timesheet/deleted` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-deleted-timesheets.md) for the provider-specific parameters and requirements.

