# Airlabs: List Real-Time Flights

Retrieves real-time flight data from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-real-time-flights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-real-time-flights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-real-time-flights?${params}`, {
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
| `airlineIata` | string | no | Filter by airline IATA code. |
| `arrIata` | string | no | Filter by arrival airport IATA code. |
| `bbox` | string | no | Bounding box as south-west latitude, south-west longitude, north-east latitude, north-east longitude. |
| `depIata` | string | no | Filter by departure airport IATA code. |
| `fields` | string | no | Comma-separated fields to return. |
| `flightIata` | string | no | Filter by flight IATA code-number, such as AA6. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aircraft_icao": "string",
      "airline_iata": "string",
      "airline_icao": "string",
      "alt": 1,
      "arr_iata": "string",
      "arr_icao": "string",
      "dep_iata": "string",
      "dep_icao": "string",
      "dir": 1,
      "flag": "string",
      "flight_iata": "string",
      "flight_icao": "string",
      "flight_number": "string",
      "hex": "string",
      "lat": 1,
      "lng": 1,
      "reg_number": "string",
      "speed": 1,
      "squawk": "string",
      "status": "string",
      "updated": 1,
      "v_speed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aircraft_icao` | string | Aircraft ICAO type code. |
| `airline_iata` | string | Airline IATA code. |
| `airline_icao` | string | Airline ICAO code. |
| `alt` | number | Current altitude. |
| `arr_iata` | string | Arrival airport IATA code. |
| `arr_icao` | string | Arrival airport ICAO code. |
| `dep_iata` | string | Departure airport IATA code. |
| `dep_icao` | string | Departure airport ICAO code. |
| `dir` | number | Current direction in degrees. |
| `flag` | string | Aircraft or airline country code. |
| `flight_iata` | string | Flight IATA code. |
| `flight_icao` | string | Flight ICAO code. |
| `flight_number` | string | Flight number. |
| `hex` | string | ICAO24 hex address. |
| `lat` | number | Current latitude. |
| `lng` | number | Current longitude. |
| `reg_number` | string | Aircraft registration number. |
| `speed` | number | Current speed. |
| `squawk` | string | Transponder squawk code. |
| `status` | string | Current flight status. |
| `updated` | number | Last update timestamp. |
| `v_speed` | number | Vertical speed. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /flights` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-real-time-flights.md) for the provider-specific parameters and requirements.

