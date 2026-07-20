# SharpAPI: Calculate Flight Duration

Retrieves flight duration details from SharpAPI.

```
GET https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/calculate-flight-duration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/calculate-flight-duration?connectionId=$CONNECTION_ID&departureCodeType=IATA&departureCode=SIN&departureDate=2024-06-27&departureTime=01%3A40&arrivalCodeType=IATA&arrivalCode=DXB&arrivalDate=2024-06-27&arrivalTime=12%3A10" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departureCodeType": "IATA",
  "departureCode": "SIN",
  "departureDate": "2024-06-27",
  "departureTime": "01:40",
  "arrivalCodeType": "IATA",
  "arrivalCode": "DXB",
  "arrivalDate": "2024-06-27",
  "arrivalTime": "12:10"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/calculate-flight-duration?${params}`, {
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
| `departureCodeType` | string | yes | Departure airport code type, such as IATA. Example: `IATA`. |
| `departureCode` | string | yes | Departure airport code. Example: `SIN`. |
| `departureDate` | string | yes | Departure local date in YYYY-MM-DD format. Example: `2024-06-27`. |
| `departureTime` | string | yes | Departure local time in HH:MM format. Example: `01:40`. |
| `arrivalCodeType` | string | yes | Arrival airport code type, such as IATA. Example: `IATA`. |
| `arrivalCode` | string | yes | Arrival airport code. Example: `DXB`. |
| `arrivalDate` | string | yes | Arrival local date in YYYY-MM-DD format. Example: `2024-06-27`. |
| `arrivalTime` | string | yes | Arrival local time in HH:MM format. Example: `12:10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "arrival_airport": {
        "name": "Ava Chen"
      },
      "arrival_local": "string",
      "departure_airport": {
        "name": "Ava Chen"
      },
      "departure_local": "string",
      "flight_length": {
        "hours": 1,
        "human": "string",
        "minutes": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `arrival_airport.name` | string | Arrival airport name. |
| `arrival_local` | string | Arrival local timestamp. |
| `departure_airport.name` | string | Departure airport name. |
| `departure_local` | string | Departure local timestamp. |
| `flight_length.hours` | number | Flight duration hours component. |
| `flight_length.human` | string | Human-readable flight duration. |
| `flight_length.minutes` | number | Flight duration minutes component. |

## Native endpoint

Through the native SharpAPI API, this operation is `GET /airports/flight_duration/:departureCodeType/:departureCode/:departureDate/:departureTime/:arrivalCodeType/:arrivalCode/:arrivalDate/:arrivalTime` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-flight-duration.md) for the provider-specific parameters and requirements.

