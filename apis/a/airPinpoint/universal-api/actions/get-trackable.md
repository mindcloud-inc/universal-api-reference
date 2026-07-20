# AirPinpoint: Get Trackable

Retrieves details for a trackable in AirPinpoint.

```
GET https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable?connectionId=$CONNECTION_ID&trackableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable?${params}`, {
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
| `trackableId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batteryInfo": {
        "batteryMonths": 1,
        "batteryPercentage": 1,
        "estimatedDaysRemaining": 1,
        "lastBatteryReset": "2026-05-07T12:00:00.000Z"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "lastKnownLocation": {
        "altitude": 1,
        "batteryLevel": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "deletedAt": "2026-05-07T12:00:00.000Z",
        "horizontalAccuracy": 1,
        "id": "string",
        "isInaccurate": true,
        "isOld": true,
        "latitude": 1,
        "longitude": 1,
        "timestamp": "2026-05-07T12:00:00.000Z",
        "trackableId": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "verticalAccuracy": 1
      },
      "model": "string",
      "name": "Ava Chen",
      "pairedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batteryInfo.batteryMonths` | number |  |
| `batteryInfo.batteryPercentage` | number |  |
| `batteryInfo.estimatedDaysRemaining` | number |  |
| `batteryInfo.lastBatteryReset` | date |  |
| `createdAt` | date |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `lastKnownLocation.altitude` | number |  |
| `lastKnownLocation.batteryLevel` | number |  |
| `lastKnownLocation.createdAt` | date |  |
| `lastKnownLocation.deletedAt` | date |  |
| `lastKnownLocation.horizontalAccuracy` | number |  |
| `lastKnownLocation.id` | string |  |
| `lastKnownLocation.isInaccurate` | boolean |  |
| `lastKnownLocation.isOld` | boolean |  |
| `lastKnownLocation.latitude` | number |  |
| `lastKnownLocation.longitude` | number |  |
| `lastKnownLocation.timestamp` | date |  |
| `lastKnownLocation.trackableId` | string |  |
| `lastKnownLocation.updatedAt` | date |  |
| `lastKnownLocation.verticalAccuracy` | number |  |
| `model` | string |  |
| `name` | string |  |
| `pairedAt` | date |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `GET /trackables/{trackableId}` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-trackable.md) for the provider-specific parameters and requirements.

