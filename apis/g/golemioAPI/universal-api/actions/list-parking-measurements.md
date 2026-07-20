# Golemio API: List Parking Measurements

Finds parking measurements in the Golemio API.

```
GET https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-measurements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Golemio API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-measurements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/golemioAPI/latest/actions/list-parking-measurements?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "closedSpotNumber": 1,
      "freeSpotNumber": 1,
      "hasFreeSpots": true,
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "occupiedSpotNumber": 1,
      "parkingId": "string",
      "primarySource": "string",
      "primarySourceId": "string",
      "totalSpotNumber": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closedSpotNumber` | number | Closed spaces. |
| `freeSpotNumber` | number | Available spaces. |
| `hasFreeSpots` | boolean | Whether free-spot data is available. |
| `lastUpdated` | date | Measurement update time. |
| `occupiedSpotNumber` | number | Occupied spaces. |
| `parkingId` | string | Parking location identifier. |
| `primarySource` | string | Source system for the measurement. |
| `primarySourceId` | string | Source-specific parking identifier. |
| `totalSpotNumber` | number | Total number of parking spaces. |

## Native endpoint

Through the native Golemio API API, this operation is `GET /v3/parking-measurements` (base URL `https://api.golemio.cz`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-parking-measurements.md) for the provider-specific parameters and requirements.

