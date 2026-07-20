# BambooHR: Add Time Off Request

Creates a time off request for an employee in BambooHR.

```
POST https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/add-time-off-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BambooHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/add-time-off-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeId": "4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bambooHrV2/latest/actions/add-time-off-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeId": "4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeId` | string | yes | The BambooHR employee identifier for the time-off request. Example: `4`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BambooHR API returns.

## Native endpoint

Through the native BambooHR API, this operation is `PUT /v1/employees/:employeeId/time_off/request` (base URL `https://mindcloud.bamboohr.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-time-off-request.md) for the provider-specific parameters and requirements.

