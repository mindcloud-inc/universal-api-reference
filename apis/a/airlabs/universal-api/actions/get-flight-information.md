# Airlabs: Get Flight Information

Retrieves current flight information from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/get-flight-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/get-flight-information?connectionId=$CONNECTION_ID&flightIata=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "flightIata": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/get-flight-information?${params}`, {
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
| `flightIata` | string | yes | Search by flight IATA code-number, such as AA6. Use this unless you have the ICAO code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flightIcao` | string | no | Alternative search by flight ICAO code-number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aircraft_icao": "string",
      "airline_iata": "string",
      "airline_icao": "string",
      "airline_name": "Ava Chen",
      "arr_actual": "string",
      "arr_actual_ts": 1,
      "arr_actual_utc": "string",
      "arr_baggage": "string",
      "arr_city": "string",
      "arr_country": "string",
      "arr_delayed": 1,
      "arr_estimated": "string",
      "arr_estimated_ts": 1,
      "arr_estimated_utc": "string",
      "arr_gate": "string",
      "arr_iata": "string",
      "arr_icao": "string",
      "arr_name": "Ava Chen",
      "arr_terminal": "string",
      "arr_time": "string",
      "arr_time_ts": 1,
      "arr_time_utc": "string",
      "cs_airline_iata": "string",
      "cs_flight_iata": "string",
      "cs_flight_number": "string",
      "delayed": 1,
      "dep_actual": "string",
      "dep_actual_ts": 1,
      "dep_actual_utc": "string",
      "dep_city": "string",
      "dep_country": "string",
      "dep_delayed": 1,
      "dep_estimated": "string",
      "dep_estimated_ts": 1,
      "dep_estimated_utc": "string",
      "dep_gate": "string",
      "dep_iata": "string",
      "dep_icao": "string",
      "dep_name": "Ava Chen",
      "dep_terminal": "string",
      "dep_time": "string",
      "dep_time_ts": 1,
      "dep_time_utc": "string",
      "duration": 1,
      "flag": "string",
      "flight_iata": "string",
      "flight_icao": "string",
      "flight_number": "string",
      "percent": 1,
      "reg_number": "string",
      "status": "string",
      "updated": 1,
      "utc": "string"
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
| `airline_name` | string | Airline name. |
| `arr_actual` | string | Actual arrival time. |
| `arr_actual_ts` | number | Actual arrival timestamp. |
| `arr_actual_utc` | string | Actual arrival time in UTC. |
| `arr_baggage` | string | Arrival baggage belt. |
| `arr_city` | string | Arrival city. |
| `arr_country` | string | Arrival country. |
| `arr_delayed` | number | Arrival delay in minutes. |
| `arr_estimated` | string | Estimated arrival time. |
| `arr_estimated_ts` | number | Estimated arrival timestamp. |
| `arr_estimated_utc` | string | Estimated arrival time in UTC. |
| `arr_gate` | string | Arrival gate. |
| `arr_iata` | string | Arrival airport IATA code. |
| `arr_icao` | string | Arrival airport ICAO code. |
| `arr_name` | string | Arrival airport name. |
| `arr_terminal` | string | Arrival terminal. |
| `arr_time` | string | Scheduled arrival time. |
| `arr_time_ts` | number | Scheduled arrival timestamp. |
| `arr_time_utc` | string | Scheduled arrival time in UTC. |
| `cs_airline_iata` | string | Codeshare airline IATA code. |
| `cs_flight_iata` | string | Codeshare flight IATA code. |
| `cs_flight_number` | string | Codeshare flight number. |
| `delayed` | number | Deprecated delay value. |
| `dep_actual` | string | Actual departure time. |
| `dep_actual_ts` | number | Actual departure timestamp. |
| `dep_actual_utc` | string | Actual departure time in UTC. |
| `dep_city` | string | Departure city. |
| `dep_country` | string | Departure country. |
| `dep_delayed` | number | Departure delay in minutes. |
| `dep_estimated` | string | Estimated departure time. |
| `dep_estimated_ts` | number | Estimated departure timestamp. |
| `dep_estimated_utc` | string | Estimated departure time in UTC. |
| `dep_gate` | string | Departure gate. |
| `dep_iata` | string | Departure airport IATA code. |
| `dep_icao` | string | Departure airport ICAO code. |
| `dep_name` | string | Departure airport name. |
| `dep_terminal` | string | Departure terminal. |
| `dep_time` | string | Scheduled departure time. |
| `dep_time_ts` | number | Scheduled departure timestamp. |
| `dep_time_utc` | string | Scheduled departure time in UTC. |
| `duration` | number | Flight duration. |
| `flag` | string | Airline country code. |
| `flight_iata` | string | Flight IATA code. |
| `flight_icao` | string | Flight ICAO code. |
| `flight_number` | string | Flight number. |
| `percent` | number | Flight progress percentage. |
| `reg_number` | string | Aircraft registration number. |
| `status` | string | Current flight status. |
| `updated` | number | Last update timestamp. |
| `utc` | string | AirLabs UTC marker. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /flight` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flight-information.md) for the provider-specific parameters and requirements.

