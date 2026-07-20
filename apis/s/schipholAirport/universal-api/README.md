# <img src="https://images.mindcloud.co/apps/icons/favicon-nationalize-io-48x48_1777546332879.png" alt="Schiphol Airport logo" width="28" height="28"> Schiphol Airport: Universal API

Access Amsterdam Airport Schiphol public flight information, including flights, airlines, aircraft types, destinations, and flight status data from the Public Flight API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/schipholAirport/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.schiphol.nl/en/developer-center/
- **Vendor API docs:** https://developer.schiphol.nl/apis/flight-api/v4/quickstarts

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Flights](actions/list-flights.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Aircraft Type

| Action | Method | Description |
| --- | --- | --- |
| [List Aircraft Types](actions/list-aircraft-types.md) | GET | Retrieves aircraft types from Schiphol Airport. |

### Airline

| Action | Method | Description |
| --- | --- | --- |
| [Get Airline](actions/get-airline.md) | GET | Retrieves an airline from Schiphol Airport by IATA or ICAO code. |
| [List Airlines](actions/list-airlines.md) | GET | Retrieves a list of airlines from Schiphol Airport. |

### Destination

| Action | Method | Description |
| --- | --- | --- |
| [Get Destination](actions/get-destination.md) | GET | Retrieves a destination from Schiphol Airport by IATA code. |
| [List Destinations](actions/list-destinations.md) | GET | Retrieves a list of destinations from Schiphol Airport. |

### Flight

| Action | Method | Description |
| --- | --- | --- |
| [Get Flight](actions/get-flight.md) | GET | Retrieves a flight from Schiphol Airport by flight ID. |
| [List Flights](actions/list-flights.md) | GET | Retrieves flights from Schiphol Airport for a specific date. |

### Flight Id

| Action | Method | Description |
| --- | --- | --- |
| [List Flight IDs](actions/list-flight-ids.md) | GET | Retrieves flight IDs from Schiphol Airport by datetime range. |

