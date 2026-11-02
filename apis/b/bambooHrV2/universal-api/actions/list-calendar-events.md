# BambooHR: List Calendar Events

Lists calendar events from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-calendar-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-calendar-events?connectionId=$CONNECTION_ID&limit=25&offset=0&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "start": "2026-05-07T12:00:00.000Z",
  "end": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-calendar-events?${params}`, {
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
| `start` | date | yes | Inclusive start date (YYYY-MM-DD). Interpreted in the company timezone. |
| `end` | date | yes | Inclusive end date (YYYY-MM-DD). Must be on or after start; the range must span less than one year. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | OData filter expression applied to calendar events. Supported operators: `eq` (equals), `in` (value in list), `and` (combine clauses). Filterable fields: `type` (one of `TIME_OFF`, `HOLIDAY`, `BIRTHDAY`, `ANNIVERSARY`), `employeeId` (int), `department` (int), `division` (int), `location` (int). Per-employee filters have no effect on HOLIDAY events. Example: `type in ('TIME_OFF','HOLIDAY') and department in (10,20)`. |
| `directReportsOnly` | boolean | no | When true, restrict employee-bound events to the caller's direct reports. HOLIDAY events are unaffected. Callers with no direct reports receive an empty result for employee-bound types. Default: `false`. |
| `includePersons` | boolean | no | When true, embed a persons map (keyed by employee id) alongside the events. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/calendar-events` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calendar-events.md) for the provider-specific parameters and requirements.

