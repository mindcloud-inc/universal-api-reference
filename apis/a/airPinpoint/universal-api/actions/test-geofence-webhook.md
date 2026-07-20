# AirPinpoint: Test Geofence Webhook

Sends a test geofence webhook from AirPinpoint.

```
POST https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/test-geofence-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/test-geofence-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventType": "string",
  "geofenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/test-geofence-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventType": "string",
    "geofenceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventType` | string | yes |  |
| `geofenceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliveryId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliveryId` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `POST /geofences/{geofence_id}/test-webhook` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-geofence-webhook.md) for the provider-specific parameters and requirements.

