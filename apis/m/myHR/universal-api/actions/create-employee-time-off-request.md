# MyHR: Create Employee Time Off Request



```
POST https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee-time-off-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee-time-off-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeePid": "string",
  "company_timeoff_reason.pid": "string",
  "employee_timeoff_request_days[].date": "string",
  "employee_timeoff_request_days[].num_hours": 1,
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/create-employee-time-off-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeePid": "string",
    "company_timeoff_reason.pid": "string",
    "employee_timeoff_request_days[].date": "string",
    "employee_timeoff_request_days[].num_hours": 1,
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeePid` | string | yes | The employee PID to create the time off request for. |
| `company_timeoff_reason.pid` | string | yes | The company time off reason PID to apply to the request. |
| `employee_timeoff_request_days[].date` | string | yes | The date for one requested time off day in YYYY-MM-DD format, for example 2026-03-31. |
| `employee_timeoff_request_days[].num_hours` | number | yes | The number of hours requested for one time off day, for example 8. |
| `status` | string | yes | The initial time off request status tag, for example TO_REVIEW. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyTimeoffReason": {
        "dateCreation": "string",
        "dateLastAction": "string",
        "dateLastUpdate": "string",
        "label": "string",
        "object": "string",
        "pid": "string"
      },
      "dateCreation": "string",
      "dateLastAction": "string",
      "dateLastUpdate": "string",
      "employee": {
        "foreignKey": "string",
        "isPartial": true,
        "object": "string",
        "pid": "string"
      },
      "endDate": "string",
      "numHours": 1,
      "object": "string",
      "pid": "string",
      "startDate": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyTimeoffReason.dateCreation` | string |  |
| `companyTimeoffReason.dateLastAction` | string |  |
| `companyTimeoffReason.dateLastUpdate` | string |  |
| `companyTimeoffReason.label` | string |  |
| `companyTimeoffReason.object` | string |  |
| `companyTimeoffReason.pid` | string |  |
| `dateCreation` | string |  |
| `dateLastAction` | string |  |
| `dateLastUpdate` | string |  |
| `employee.foreignKey` | string |  |
| `employee.isPartial` | boolean |  |
| `employee.object` | string |  |
| `employee.pid` | string |  |
| `endDate` | string |  |
| `numHours` | number |  |
| `object` | string |  |
| `pid` | string |  |
| `startDate` | string |  |
| `status` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `POST /employees/:employee_pid/employee_timeoff_request` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee-time-off-request.md) for the provider-specific parameters and requirements.

