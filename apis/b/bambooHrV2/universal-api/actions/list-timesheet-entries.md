# BambooHR: List Timesheet Entries

Lists timesheet entries from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-timesheet-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-timesheet-entries?connectionId=$CONNECTION_ID&start=2025-01-01&end=2025-03-01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "2025-01-01",
  "end": "2025-03-01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-timesheet-entries?${params}`, {
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
| `start` | date | yes | YYYY-MM-DD. Only show timesheet entries on/after the specified start date. Must be within the last 365 days. Example: `2025-01-01`. |
| `end` | date | yes | YYYY-MM-DD. Only show timesheet entries on/before the specified end date. Must be within the last 365 days. Example: `2025-03-01`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeIds` | string | no | A comma-separated list of internal employee IDs. When specified, only entries that match these employee IDs are returned. When omitted, entries for all accessible employees are returned. Accepts multiple values in one string, delimited by `,`. Example: `1,2,3`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/time_tracking/timesheet_entries` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timesheet-entries.md) for the provider-specific parameters and requirements.

