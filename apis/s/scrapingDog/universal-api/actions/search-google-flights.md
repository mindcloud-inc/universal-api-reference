# ScrapingDog: Search Google Flights

Retrieves Google Flights search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-flights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-flights?connectionId=$CONNECTION_ID&arrivalId=string&departureId=string&outboundDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arrivalId": "string",
  "departureId": "string",
  "outboundDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-google-flights?${params}`, {
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
| `arrivalId` | string | yes | Arrival airport code or location identifier. |
| `departureId` | string | yes | Departure airport code or location identifier. |
| `outboundDate` | string | yes | Outbound travel date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airports": {
        "departure": {
          "airport": {
            "id": "string",
            "name": "Ava Chen"
          },
          "city": "string",
          "country": "string",
          "country_code": "string"
        }
      },
      "best_flights": {
        "booking_token": "string",
        "carbon_emission": {
          "difference_percent": 1,
          "this_flight": 1,
          "typical_for_this_route": 1
        },
        "flights": {
          "airline": "string",
          "airplane": "string",
          "arrival_airport": {
            "id": "string",
            "name": "Ava Chen",
            "time": "string"
          },
          "departure_airport": {
            "id": "string",
            "name": "Ava Chen",
            "time": "string"
          },
          "duration": 1,
          "extensions": [
            "string"
          ],
          "flight_number": "string",
          "legroom": "string",
          "travel_class": "string"
        },
        "layovers": [
          "string"
        ],
        "price": 1,
        "total_duration": 1,
        "type": "string"
      },
      "other_flights": {
        "booking_token": "string",
        "carbon_emission": {
          "difference_percent": 1,
          "this_flight": 1,
          "typical_for_this_route": 1
        },
        "flights": {
          "airline": "string",
          "airplane": "string",
          "arrival_airport": {
            "id": "string",
            "name": "Ava Chen",
            "time": "string"
          },
          "departure_airport": {
            "id": "string",
            "name": "Ava Chen",
            "time": "string"
          },
          "duration": 1,
          "extensions": [
            "string"
          ],
          "flight_number": "string",
          "legroom": "string",
          "travel_class": "string"
        },
        "layovers": [
          "string"
        ],
        "price": 1,
        "total_duration": 1,
        "type": "string"
      },
      "price_insights": {
        "lowest_price": 1,
        "price_history": [
          [
            "string"
          ]
        ],
        "typical_price_range": [
          1
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airports` | array<object> |  |
| `airports.departure` | array<object> |  |
| `airports.departure.airport` | object |  |
| `airports.departure.airport.id` | string |  |
| `airports.departure.airport.name` | string |  |
| `airports.departure.city` | string |  |
| `airports.departure.country` | string |  |
| `airports.departure.country_code` | string |  |
| `best_flights` | array<object> |  |
| `best_flights.booking_token` | string |  |
| `best_flights.carbon_emission` | object |  |
| `best_flights.carbon_emission.difference_percent` | number |  |
| `best_flights.carbon_emission.this_flight` | number |  |
| `best_flights.carbon_emission.typical_for_this_route` | number |  |
| `best_flights.flights` | array<object> |  |
| `best_flights.flights.airline` | string |  |
| `best_flights.flights.airplane` | string |  |
| `best_flights.flights.arrival_airport` | object |  |
| `best_flights.flights.arrival_airport.id` | string |  |
| `best_flights.flights.arrival_airport.name` | string |  |
| `best_flights.flights.arrival_airport.time` | string |  |
| `best_flights.flights.departure_airport` | object |  |
| `best_flights.flights.departure_airport.id` | string |  |
| `best_flights.flights.departure_airport.name` | string |  |
| `best_flights.flights.departure_airport.time` | string |  |
| `best_flights.flights.duration` | number |  |
| `best_flights.flights.extensions` | array<string> |  |
| `best_flights.flights.flight_number` | string |  |
| `best_flights.flights.legroom` | string |  |
| `best_flights.flights.travel_class` | string |  |
| `best_flights.layovers` | array<string> |  |
| `best_flights.price` | number |  |
| `best_flights.total_duration` | number |  |
| `best_flights.type` | string |  |
| `other_flights` | array<object> |  |
| `other_flights.booking_token` | string |  |
| `other_flights.carbon_emission` | object |  |
| `other_flights.carbon_emission.difference_percent` | number |  |
| `other_flights.carbon_emission.this_flight` | number |  |
| `other_flights.carbon_emission.typical_for_this_route` | number |  |
| `other_flights.flights` | array<object> |  |
| `other_flights.flights.airline` | string |  |
| `other_flights.flights.airplane` | string |  |
| `other_flights.flights.arrival_airport` | object |  |
| `other_flights.flights.arrival_airport.id` | string |  |
| `other_flights.flights.arrival_airport.name` | string |  |
| `other_flights.flights.arrival_airport.time` | string |  |
| `other_flights.flights.departure_airport` | object |  |
| `other_flights.flights.departure_airport.id` | string |  |
| `other_flights.flights.departure_airport.name` | string |  |
| `other_flights.flights.departure_airport.time` | string |  |
| `other_flights.flights.duration` | number |  |
| `other_flights.flights.extensions` | array<string> |  |
| `other_flights.flights.flight_number` | string |  |
| `other_flights.flights.legroom` | string |  |
| `other_flights.flights.travel_class` | string |  |
| `other_flights.layovers` | array<string> |  |
| `other_flights.price` | number |  |
| `other_flights.total_duration` | number |  |
| `other_flights.type` | string |  |
| `price_insights` | object |  |
| `price_insights.lowest_price` | number |  |
| `price_insights.price_history` | array<array> |  |
| `price_insights.typical_price_range` | array<number> |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_flights` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-flights.md) for the provider-specific parameters and requirements.

