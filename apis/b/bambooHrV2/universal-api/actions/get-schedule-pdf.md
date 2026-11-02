# BambooHR: Get Schedule PDF

Retrieves schedule pdf from BambooHR.

```
GET https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-schedule-pdf
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-schedule-pdf?connectionId=$CONNECTION_ID&id=string&startYmd=2026-05-07T12%3A00%3A00.000Z&endYmd=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "startYmd": "2026-05-07T12:00:00.000Z",
  "endYmd": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/get-schedule-pdf?${params}`, {
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
| `id` | string | yes | The schedule ID |
| `startYmd` | date | yes | Start date in YYYY-MM-DD format |
| `endYmd` | date | yes | End date in YYYY-MM-DD format |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupBy` | list<string> | no | Group employees by this field One of: `department`, `division`, `jobTitle`, `location`, `team`. |
| `employeeIds` | string | no | Filter by employee IDs. Pass the string "null" as an element to include open shifts. Accepts multiple values as an array. |
| `includeEmployeesWithoutShifts` | boolean | no | Whether to include employees who have no shifts in the date range Default: `false`. |
| `includeHolidays` | boolean | no | Whether to include holidays in the PDF Default: `false`. |
| `includeTimeOff` | boolean | no | Whether to include time-off entries in the PDF Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `GET /v1/scheduling/schedules/:id/pdf` (base URL `https://{{credentials.companyDomain}}.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schedule-pdf.md) for the provider-specific parameters and requirements.

