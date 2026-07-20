# Vouchsafe: Toggle Alerts

Updates ongoing monitoring for an alert account in Vouchsafe.

```
PUT https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/toggle-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchsafe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/toggle-alerts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "alertsEnabled": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vouchsafe/latest/actions/toggle-alerts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "alertsEnabled": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The monitored account ID (Smart Lookup ID). |
| `alertsEnabled` | boolean | yes | Whether to enable or disable ongoing monitoring for this account. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Vouchsafe API returns.

## Native endpoint

Through the native Vouchsafe API, this operation is `PATCH /alerts/accounts/:id` (base URL `https://app.vouchsafe.id/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/toggle-alerts.md) for the provider-specific parameters and requirements.

