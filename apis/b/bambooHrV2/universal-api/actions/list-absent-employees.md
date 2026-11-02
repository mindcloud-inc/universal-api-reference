# BambooHR: List Absent Employees

Lists absent employees from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-absent-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-absent-employees?connectionId=$CONNECTION_ID&limit=25&offset=0&start=2026-05-07T12%3A00%3A00.000Z&end=2026-05-07T12%3A00%3A00.000Z" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/list-absent-employees?${params}`, {
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
| `end` | date | yes | Inclusive end date (YYYY-MM-DD). Must be on or after start; the range may not exceed 366 days. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filter` | string | no | OData filter expression applied to who's out results. Supported operators: `eq` (equals), `in` (value in list), `and` (combine clauses). Filterable fields: `employeeId` (int), `department` (int), `division` (int), `location` (int). Examples: `employeeId eq 42`, `department in (10, 20) and location eq 5`. |
| `directReportsOnly` | boolean | no | When true, restrict to time off for the caller's direct reports. Callers with no direct reports receive an empty result. Default: `false`. |
| `includePersons` | boolean | no | When true, embed a persons map of employee display data alongside results. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employeeId": 1,
      "end": "string",
      "id": "string",
      "start": "string",
      "timeOffTypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employeeId` | number |  |
| `end` | string |  |
| `id` | string |  |
| `start` | string |  |
| `timeOffTypeId` | number |  |

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/whos-out` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-absent-employees.md) for the provider-specific parameters and requirements.

