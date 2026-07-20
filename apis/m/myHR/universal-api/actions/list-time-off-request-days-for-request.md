# MyHR: List Time Off Request Days For Request



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-time-off-request-days-for-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-time-off-request-days-for-request?connectionId=$CONNECTION_ID&employeeTimeoffRequestPid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeTimeoffRequestPid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/list-time-off-request-days-for-request?${params}`, {
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
| `employeeTimeoffRequestPid` | string | yes | The employee time off request PID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
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
| `numHours` | string |  |
| `object` | string |  |
| `pid` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employee_timeoff_requests/:employee_timeoff_request_pid/employee_timeoff_request_days` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-off-request-days-for-request.md) for the provider-specific parameters and requirements.

