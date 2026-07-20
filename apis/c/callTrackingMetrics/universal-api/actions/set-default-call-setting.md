# CallTrackingMetrics: Set Default Call Setting

Sets a default call setting in CallTrackingMetrics.

```
PUT https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/set-default-call-setting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/set-default-call-setting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "callSettingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/set-default-call-setting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "callSettingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `callSettingId` | string | yes | The CallTrackingMetrics call setting ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `PATCH /accounts/:accountId/call_settings/:callSettingId/set_default` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-default-call-setting.md) for the provider-specific parameters and requirements.

