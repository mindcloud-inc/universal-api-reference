# Zenoti: List Center Employee Schedules



```
GET https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-employee-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zenoti `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-employee-schedules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zenoti/latest/actions/list-center-employee-schedules?${params}`, {
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
| `centerId` | list | no |  |
| `startDate` | date | no |  |
| `endDate` | date | no |  |
| `scheduleStatus` | list | no |  |
| `employeeId` | string | no |  |
| `considerScheduleTime` | boolean | no | If true, the API considers the time stamp for the specified date range to filter the response data. If false, the API considers only the date values to filter the employee schedules. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employeeId": "string",
      "employeeName": "Ava Chen",
      "schedules": [
        {
          "date": "string",
          "shifts": [
            {
              "endTime": "string",
              "roomId": "string",
              "scheduleId": "string",
              "startTime": "string",
              "status": 1
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employeeId` | string |  |
| `employeeName` | string |  |
| `schedules[].date` | string |  |
| `schedules[].shifts[].endTime` | string |  |
| `schedules[].shifts[].roomId` | string |  |
| `schedules[].shifts[].scheduleId` | string |  |
| `schedules[].shifts[].startTime` | string |  |
| `schedules[].shifts[].status` | number |  |

## Native endpoint

Through the native Zenoti API, this operation is `GET centers/:centerId/employee_schedules` (base URL `https://api.zenoti.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-center-employee-schedules.md) for the provider-specific parameters and requirements.

