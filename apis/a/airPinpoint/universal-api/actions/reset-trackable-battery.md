# AirPinpoint: Reset Trackable Battery

Resets the battery counter for a trackable in AirPinpoint.

```
PUT https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/reset-trackable-battery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/reset-trackable-battery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "batteryMonths": 1,
  "trackableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/reset-trackable-battery', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "batteryMonths": 1,
    "trackableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `batteryMonths` | number | yes |  |
| `trackableId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `POST /trackables/{trackableId}/battery` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-trackable-battery.md) for the provider-specific parameters and requirements.

