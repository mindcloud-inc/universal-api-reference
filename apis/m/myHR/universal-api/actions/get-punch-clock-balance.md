# MyHR: Get Punch Clock Balance



```
GET https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-punch-clock-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MyHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-punch-clock-balance?connectionId=$CONNECTION_ID&employeePid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeePid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/myHR/latest/actions/get-punch-clock-balance?${params}`, {
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
      "balance": 1,
      "balanceGross": 1,
      "considered": {
        "end": "string",
        "start": "string"
      },
      "considerUntil": "string",
      "period": {
        "end": "string",
        "start": "string"
      },
      "policy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number |  |
| `balanceGross` | number |  |
| `considered.end` | string |  |
| `considered.start` | string |  |
| `considerUntil` | string |  |
| `period.end` | string |  |
| `period.start` | string |  |
| `policy` | string |  |

## Native endpoint

Through the native MyHR API, this operation is `GET /employees/:employee_pid/punch-clock/balance` (base URL `https://mindcloud.myhr.lu/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-punch-clock-balance.md) for the provider-specific parameters and requirements.

