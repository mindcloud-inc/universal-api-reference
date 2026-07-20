# AirPinpoint: Create Geofence

Creates a geofence for AirPinpoint trackables.

```
POST https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/create-geofence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/create-geofence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "latitude": 1,
  "longitude": 1,
  "name": "Ava Chen",
  "radius": 1,
  "trackableId[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/create-geofence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "latitude": 1,
    "longitude": 1,
    "name": "Ava Chen",
    "radius": 1,
    "trackableId[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `latitude` | number | yes |  |
| `longitude` | number | yes |  |
| `name` | string | yes |  |
| `notifyDestination` | string | no |  |
| `notifyType` | string | no |  |
| `radius` | number | yes |  |
| `trackableId[]` | array<string> | yes |  |
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

Through the native AirPinpoint API, this operation is `POST /geofences` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-geofence.md) for the provider-specific parameters and requirements.

