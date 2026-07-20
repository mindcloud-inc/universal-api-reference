# AirPinpoint: Update Geofence

Updates an existing geofence in AirPinpoint.

```
PUT https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/update-geofence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/update-geofence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "geofenceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/update-geofence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "geofenceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `geofenceId` | string | yes |  |
| `latitude` | number | no |  |
| `longitude` | number | no |  |
| `name` | string | no |  |
| `notifyDestination` | string | no |  |
| `notifyType` | string | no |  |
| `radius` | number | no |  |
| `trackableId[]` | array<string> | no |  |
| `webhookEnabled` | boolean | no |  |
| `webhookSecret` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authUserId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "notifyDestination": "string",
      "notifyType": "string",
      "radius": 1,
      "trackableId": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhookEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authUserId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `notifyDestination` | string |  |
| `notifyType` | string |  |
| `radius` | number |  |
| `trackableId` | array<string> |  |
| `updatedAt` | date |  |
| `webhookEnabled` | boolean |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `PATCH /geofences/{geofence_id}` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-geofence.md) for the provider-specific parameters and requirements.

