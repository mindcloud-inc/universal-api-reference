# Schiphol Airport: Get Flight

Retrieves a flight from Schiphol Airport by flight ID.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-flight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-flight?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-flight?${params}`, {
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
| `id` | string | yes | Unique numeric Schiphol flight ID. |

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
| `flightName` | string |  |
| `flightNumber` | number |  |
| `gate` | string |  |
| `id` | string |  |
| `lastUpdatedAt` | date |  |
| `pier` | string |  |
| `publicFlightState` | object |  |
| `route` | object |  |
| `scheduleDate` | date |  |
| `scheduleDateTime` | date |  |
| `scheduleTime` | string |  |
| `terminal` | number |  |

## Native endpoint

Through the native Schiphol Airport API, this operation is `GET /flights/:id` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-flight.md) for the provider-specific parameters and requirements.

