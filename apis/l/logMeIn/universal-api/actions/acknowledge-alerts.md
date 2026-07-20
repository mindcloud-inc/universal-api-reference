# LogMeIn: Acknowledge Alerts

Updates alerts by acknowledging them in LogMeIn.

```
PUT https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/acknowledge-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/acknowledge-alerts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "acknowledgeData[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/acknowledge-alerts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "acknowledgeData[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `acknowledgeData[]` | array<object> | yes | Array of alert/device pairs to acknowledge. GoTo documents a maximum of 100 items. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acknowledged": true,
      "alertId": "string",
      "deviceId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acknowledged` | boolean |  |
| `alertId` | string |  |
| `deviceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve-alerts/v1/acknowledge` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/acknowledge-alerts.md) for the provider-specific parameters and requirements.

