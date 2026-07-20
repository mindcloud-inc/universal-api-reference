# AirPinpoint: List Geofences

Retrieves configured geofences for AirPinpoint trackables.

```
GET https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/list-geofences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/list-geofences?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/list-geofences?${params}`, {
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
| `trackableId` | string | no |  |

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
      "radius": 1,
      "trackableId": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
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
| `radius` | number |  |
| `trackableId` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native AirPinpoint API, this operation is `GET /geofences` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-geofences.md) for the provider-specific parameters and requirements.

