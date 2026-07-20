# Schiphol Airport: List Flights

Retrieves flights from Schiphol Airport for a specific date.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-flights?${params}`, {
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
| `scheduleDate` | date | no | Scheduled date to retrieve flights for, formatted YYYY-MM-DD. |
| `scheduleTime` | string | no | Scheduled time to retrieve flights from, formatted HH:mm. |
| `flightName` | string | no | Flight number as printed on the ticket, such as KL1234. |
| `flightDirection` | string | no | Flight direction: A for arrivals or D for departures. One of: `0`, `1`. |
| `airline` | string | no | IATA or ICAO airline prefix, such as KL or KLM. |
| `airlineCode` | number | no | Schiphol numeric airline code. |
| `route` | string | no | IATA or ICAO route airport code; multiple values can be comma separated. |
| `includedelays` | boolean | no | Include earlier scheduled flights delayed into the requested date. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Result page number, starting at 0. Default: `0`. |
| `sort` | string | no | Sort expression such as +scheduleTime or -scheduleDate,+scheduleTime. Default: `+scheduleTime`. |
| `fromDateTime` | string | no | Start of a DateTime search range, formatted yyyy-MM-ddTHH:mm:ss. |
| `toDateTime` | string | no | End of a DateTime search range, formatted yyyy-MM-ddTHH:mm:ss. |
| `searchDateTimeField` | string | no | DateTime field to query when using fromDateTime and toDateTime. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `fromScheduleDate` | date | no | Start scheduled date for a scheduleDate range, formatted YYYY-MM-DD. |
| `toScheduleDate` | date | no | End scheduled date for a scheduleDate range, formatted YYYY-MM-DD. |
| `isOperationalFlight` | boolean | no | Filter by operational or non-operational flights. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aircraftRegistration": "string",
      "aircraftType": {},
      "baggageClaim": {},
      "codeshares": {},
      "flightDirection": "string",
      "flightName": "Ava Chen",
      "flightNumber": 1,
      "gate": "string",
      "id": "string",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "pier": "string",
      "publicFlightState": {},
      "route": {},
      "scheduleDate": "2026-05-07T12:00:00.000Z",
      "scheduleDateTime": "2026-05-07T12:00:00.000Z",
      "scheduleTime": "string",
      "terminal": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aircraftRegistration` | string |  |
| `aircraftType` | object |  |
| `baggageClaim` | object |  |
| `codeshares` | object |  |
| `flightDirection` | string |  |
| `flightName` | string | Flight number as printed on the ticket |
| `flightNumber` | number |  |
| `gate` | string |  |
| `id` | string | Unique Schiphol flight ID |
| `lastUpdatedAt` | date |  |
| `pier` | string |  |
| `publicFlightState` | object |  |
| `route` | object |  |
| `scheduleDate` | date |  |
| `scheduleDateTime` | date |  |
| `scheduleTime` | string |  |
| `terminal` | number |  |

## Native endpoint

Through the native Schiphol Airport API, this operation is `GET /flights` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-flights.md) for the provider-specific parameters and requirements.

