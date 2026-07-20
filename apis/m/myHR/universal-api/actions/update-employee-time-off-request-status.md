# MyHR: Update Employee Time Off Request Status



```
PUT https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee-time-off-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee-time-off-request-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeTimeoffRequestPid": "string",
  "status": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myHR/latest/actions/update-employee-time-off-request-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeTimeoffRequestPid": "string",
    "status": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeTimeoffRequestPid` | string | yes | The employee time off request PID. |
| `status` | string | yes | The status tag to apply to the time off request, for example ACCEPTED. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": {
        "code": 1,
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success.code` | number |  |
| `success.message` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `PUT /employee_timeoff_requests/:employee_timeoff_request_pid/status` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee-time-off-request-status.md) for the provider-specific parameters and requirements.

