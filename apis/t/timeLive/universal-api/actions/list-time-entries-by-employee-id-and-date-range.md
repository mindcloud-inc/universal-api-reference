# TimeLive: List Time Entries By Employee Id And Date Range

Retrieves time entries from TimeLive by employee and date range.

```
GET https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-time-entries-by-employee-id-and-date-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimeLive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-time-entries-by-employee-id-and-date-range?connectionId=$CONNECTION_ID&employeeId=string&endDate=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "string",
  "endDate": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-time-entries-by-employee-id-and-date-range?${params}`, {
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
| `employeeId` | string | yes | Account employee id for the time entry range lookup. |
| `endDate` | string | yes | Range end date in YYYY-MM-DD format. |
| `startDate` | string | yes | Range start date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Message` | string |  |

## Native endpoint

Through the native TimeLive API, this operation is `GET /Timesheets/TimeEntriesByEmployeeIdAndDateRange/:employeeId/:startDate/:endDate` (base URL `https://mindcloudtl.livetecs.com/classic/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries-by-employee-id-and-date-range.md) for the provider-specific parameters and requirements.

