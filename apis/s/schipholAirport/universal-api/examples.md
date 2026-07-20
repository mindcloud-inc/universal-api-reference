# Schiphol Airport Universal API Examples

These examples use the MindCloud API key and Schiphol Airport connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Flights

Retrieves flights from Schiphol Airport for a specific date.

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

Example response:

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

See the full [List Flights action reference](actions/list-flights.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/schipholAirport/latest/actions/list-flights).
