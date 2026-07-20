# Airlabs: List Routes

Retrieves airline route data from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-routes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-routes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-routes?${params}`, {
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
| `depIata` | string | no | Filter by departure airport IATA code. |
| `flightIata` | string | no | Filter by flight IATA code-number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aircraft_icao": "string",
      "airline_iata": "string",
      "airline_icao": "string",
      "arr_iata": "string",
      "arr_icao": "string",
      "arr_terminals": [
        "string"
      ],
      "arr_time": "string",
      "arr_time_utc": "string",
      "counter": 1,
      "cs_airline_iata": "string",
      "cs_flight_iata": "string",
      "cs_flight_number": "string",
      "days": [
        "string"
      ],
      "dep_iata": "string",
      "dep_icao": "string",
      "dep_terminals": [
        "string"
      ],
      "dep_time": "string",
      "dep_time_utc": "string",
      "duration": 1,
      "flight_iata": "string",
      "flight_icao": "string",
      "flight_number": "string",
      "updated": 1
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
| `arr_iata` | string | Arrival airport IATA code. |
| `arr_icao` | string | Arrival airport ICAO code. |
| `arr_terminals` | array<string> | Arrival terminals. |
| `arr_time` | string | Arrival time. |
| `arr_time_utc` | string | Arrival time in UTC. |
| `counter` | number | Route counter. |
| `cs_airline_iata` | string | Codeshare airline IATA code. |
| `cs_flight_iata` | string | Codeshare flight IATA code. |
| `cs_flight_number` | string | Codeshare flight number. |
| `days` | array<string> | Days of operation. |
| `dep_iata` | string | Departure airport IATA code. |
| `dep_icao` | string | Departure airport ICAO code. |
| `dep_terminals` | array<string> | Departure terminals. |
| `dep_time` | string | Departure time. |
| `dep_time_utc` | string | Departure time in UTC. |
| `duration` | number | Flight duration. |
| `flight_iata` | string | Flight IATA code. |
| `flight_icao` | string | Flight ICAO code. |
| `flight_number` | string | Flight number. |
| `updated` | number | Last update timestamp. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /routes` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-routes.md) for the provider-specific parameters and requirements.

