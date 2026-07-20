# Float: Get People Report

Retrieves a people report from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/get-people-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/get-people-report?connectionId=$CONNECTION_ID&startDate=string&endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/get-people-report?${params}`, {
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
| `startDate` | string | yes | Start date of the report duration in the format YYYY-MM-DD |
| `endDate` | string | yes | End date of the report duration in the format YYYY-MM-DD |
| `peopleId` | number | no | A people ID to filter the response on |

## Response

```json
{
  "success": true,
  "data": [
    {
      "people": [
        {
          "billable": 1,
          "capacity": 1,
          "coHours": "string",
          "coHoursHistory": {},
          "defaultHourlyRate": {},
          "department": {},
          "departmentId": {},
          "employeeType": 1,
          "myHours": {},
          "myHoursHistory": {},
          "name": "Ava Chen",
          "nonBillable": 1,
          "overtime": 1,
          "peopleId": 1,
          "peopleTypeId": 1,
          "scheduled": 1,
          "timeoff": 1,
          "unscheduled": 1,
          "wkDayHrs": {
            "1970-01-01": [
              1
            ]
          }
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
| `people[].billable` | number |  |
| `people[].capacity` | number |  |
| `people[].coHours` | string |  |
| `people[].coHoursHistory` | object |  |
| `people[].defaultHourlyRate` | object |  |
| `people[].department` | object |  |
| `people[].departmentId` | object |  |
| `people[].employeeType` | number |  |
| `people[].myHours` | object |  |
| `people[].myHoursHistory` | object |  |
| `people[].name` | string |  |
| `people[].nonBillable` | number |  |
| `people[].overtime` | number |  |
| `people[].peopleId` | number |  |
| `people[].peopleTypeId` | number |  |
| `people[].scheduled` | number |  |
| `people[].timeoff` | number |  |
| `people[].unscheduled` | number |  |
| `people[].wkDayHrs.1970-01-01[]` | number |  |

## Native endpoint

Through the native Float API, this operation is `GET /reports/people` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-people-report.md) for the provider-specific parameters and requirements.

