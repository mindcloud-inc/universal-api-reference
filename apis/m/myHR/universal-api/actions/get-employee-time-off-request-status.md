# MyHR: Get Employee Time Off Request Status



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-time-off-request-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-time-off-request-status?connectionId=$CONNECTION_ID&employeeTimeoffRequestPid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeTimeoffRequestPid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-employee-time-off-request-status?${params}`, {
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
      "id": "string",
      "label": "string",
      "object": "string",
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `label` | string |  |
| `object` | string |  |
| `tag` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employee_timeoff_requests/:employee_timeoff_request_pid/status` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-time-off-request-status.md) for the provider-specific parameters and requirements.

