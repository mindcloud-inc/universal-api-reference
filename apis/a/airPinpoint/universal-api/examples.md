# AirPinpoint Universal API Examples

These examples use the MindCloud API key and AirPinpoint connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Trackables

Retrieves trackable devices linked to AirPinpoint.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/list-trackables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/list-trackables?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

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

See the full [List Trackables action reference](actions/list-trackables.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airPinpoint/latest/actions/list-trackables).

## Create Geofence

Creates a geofence for AirPinpoint trackables.

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

Example response:

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

See the full [Create Geofence action reference](actions/create-geofence.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airPinpoint/latest/actions/create-geofence).
