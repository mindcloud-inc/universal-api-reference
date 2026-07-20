# AirPinpoint: Get Trackable Locations

Retrieves location data for a trackable in AirPinpoint.

```
GET https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable-locations?connectionId=$CONNECTION_ID&limit=25&offset=0&trackableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "trackableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/get-trackable-locations?${params}`, {
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
| `limit` | number | no |  |
| `skip` | number | no |  |
| `trackableId` | string | yes |  |
| `startTime` | date | no | Optional ISO 8601 UTC start of the history window. |
| `endTime` | date | no | Optional ISO 8601 UTC end of the history window. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `altitude` | number |  |
| `batteryLevel` | number |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `horizontalAccuracy` | number |  |
| `id` | string |  |
| `isInaccurate` | boolean |  |
| `isOld` | boolean |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `timestamp` | date |  |
| `trackableId` | string |  |
| `updatedAt` | date |  |
| `verticalAccuracy` | number |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `GET /trackables/{trackableId}/locations` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-trackable-locations.md) for the provider-specific parameters and requirements.

