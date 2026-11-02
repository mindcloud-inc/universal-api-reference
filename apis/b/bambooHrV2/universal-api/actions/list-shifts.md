# BambooHR: List Shifts

Lists shifts from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-shifts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-shifts?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ids` | string | no | Filter by shift IDs, as either a comma-separated string (e.g. id1,id2) or an array. If provided, other filters are ignored. Accepts multiple values in one string, delimited by `,`. |
| `start` | date | no | Start datetime for the shift window (ISO-8601 datetime string). Required if ids not provided. |
| `end` | date | no | End datetime for the shift window (ISO-8601 datetime string). Required if ids not provided. |
| `employeeIds` | string | no | Filter by employee IDs, as either a comma-separated string (e.g. 10,20) or an array. Use the string "null" as a value to include unassigned shifts (e.g. employeeIds=10,null). Accepts multiple values in one string, delimited by `,`. |
| `scheduleIds` | string | no | Filter by schedule IDs, as either a comma-separated string (e.g. id1,id2) or an array. Accepts multiple values in one string, delimited by `,`. |
| `statuses` | list<string> | no | Filter by shift statuses, as either a comma-separated string (e.g. planned,published) or an array. One of: `cancelled`, `deleted`, `planned`, `published`. Accepts multiple values in one string, delimited by `,`. Default: `planned,published`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/scheduling/shifts` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shifts.md) for the provider-specific parameters and requirements.

