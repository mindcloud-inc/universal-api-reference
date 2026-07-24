# Rillion Prime Pay: Create Payment Schedule



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-schedule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "interval": "Daily"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-schedule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "interval": "Daily"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xCorrelationId` | string | no |  |
| `interval` | list<string> | yes | Interval type One of: `Daily`, `Instant`, `Weekly`. |
| `intervalConfiguration` | object | no | Configuration for interval. Required when interval is Daily or Weekly. |
| `intervalConfiguration.time` | string | no | Time of day (HH:mm:ss). Required when interval is Daily or Weekly. |
| `intervalConfiguration.day` | list<string> | no | Day of week (required when interval is Weekly). One of: `Friday`, `Monday`, `Thursday`, `Tuesday`, `Wednesday`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Pay API returns.

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/schedule` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-schedule.md) for the provider-specific parameters and requirements.

