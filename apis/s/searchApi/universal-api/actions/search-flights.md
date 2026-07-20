# SearchApi: Search Flights



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-flights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-flights?connectionId=$CONNECTION_ID&departureId=JFK&arrivalId=MAD&outboundDate=2026-04-16&returnDate=2026-04-23" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "departureId": "JFK",
  "arrivalId": "MAD",
  "outboundDate": "2026-04-16",
  "returnDate": "2026-04-23"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-flights?${params}`, {
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
| `departureId` | string | yes | Example: `JFK`. |
| `arrivalId` | string | yes | Example: `MAD`. |
| `outboundDate` | string | yes | Example: `2026-04-16`. |
| `returnDate` | string | yes | Example: `2026-04-23`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airlines": {},
      "airports": [
        {}
      ],
      "baggageAllowanceLinks": [
        {}
      ],
      "bestFlights": [
        {}
      ],
      "otherFlights": [
        {}
      ],
      "passengerAssistanceLinks": [
        {}
      ],
      "priceInsights": {},
      "searchMetadata": {},
      "searchParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airlines` | object |  |
| `airports` | array<object> |  |
| `baggageAllowanceLinks` | array<object> |  |
| `bestFlights` | array<object> |  |
| `otherFlights` | array<object> |  |
| `passengerAssistanceLinks` | array<object> |  |
| `priceInsights` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-flights.md) for the provider-specific parameters and requirements.

