# MyHR: List Time Off Request Days For Employee



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-time-off-request-days-for-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-time-off-request-days-for-employee?connectionId=$CONNECTION_ID&employeePid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeePid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-time-off-request-days-for-employee?${params}`, {
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
| `employeePid` | string | yes | The employee PID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "employeeTimeoffRequest": {
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
        "endDate": "string",
        "numHours": "string",
        "object": "string",
        "pid": "string",
        "startDate": "string",
        "status": "string"
      },
      "numHours": "string",
      "object": "string",
      "pid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `employeeTimeoffRequest.companyTimeoffReason.dateCreation` | string |  |
| `employeeTimeoffRequest.companyTimeoffReason.dateLastAction` | string |  |
| `employeeTimeoffRequest.companyTimeoffReason.dateLastUpdate` | string |  |
| `employeeTimeoffRequest.companyTimeoffReason.label` | string |  |
| `employeeTimeoffRequest.companyTimeoffReason.object` | string |  |
| `employeeTimeoffRequest.companyTimeoffReason.pid` | string |  |
| `employeeTimeoffRequest.dateCreation` | string |  |
| `employeeTimeoffRequest.dateLastAction` | string |  |
| `employeeTimeoffRequest.dateLastUpdate` | string |  |
| `employeeTimeoffRequest.endDate` | string |  |
| `employeeTimeoffRequest.numHours` | string |  |
| `employeeTimeoffRequest.object` | string |  |
| `employeeTimeoffRequest.pid` | string |  |
| `employeeTimeoffRequest.startDate` | string |  |
| `employeeTimeoffRequest.status` | string |  |
| `numHours` | string |  |
| `object` | string |  |
| `pid` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employees/:employee_pid/employee_timeoff_request_days` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-off-request-days-for-employee.md) for the provider-specific parameters and requirements.

