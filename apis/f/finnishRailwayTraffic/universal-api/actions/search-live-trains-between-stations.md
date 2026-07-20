# Finnish Railway Traffic: Search live trains between stations

Finds live trains between stations in Finnish Railway Traffic.

```
GET https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/search-live-trains-between-stations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnish Railway Traffic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/search-live-trains-between-stations?connectionId=$CONNECTION_ID&departureStation=HKI&arrivalStation=TPE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departureStation": "HKI",
  "arrivalStation": "TPE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnishRailwayTraffic/latest/actions/search-live-trains-between-stations?${params}`, {
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
| `departureStation` | string | yes | Departure station short code, for example HKI. Default: `HKI`. |
| `arrivalStation` | string | yes | Arrival station short code, for example TPE. Default: `TPE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelled": true,
      "commuterLineID": "string",
      "departureDate": "2026-05-07T12:00:00.000Z",
      "runningCurrently": true,
      "timeTableRows": [
        {}
      ],
      "trainCategory": "string",
      "trainNumber": 1,
      "trainType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled` | boolean |  |
| `commuterLineID` | string |  |
| `departureDate` | date |  |
| `runningCurrently` | boolean |  |
| `timeTableRows` | array<object> |  |
| `trainCategory` | string |  |
| `trainNumber` | number |  |
| `trainType` | string |  |

## Native endpoint

Through the native Finnish Railway Traffic API, this operation is `GET /api/v1/live-trains/station/:departure_station/:arrival_station` (base URL `https://rata.digitraffic.fi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-live-trains-between-stations.md) for the provider-specific parameters and requirements.

