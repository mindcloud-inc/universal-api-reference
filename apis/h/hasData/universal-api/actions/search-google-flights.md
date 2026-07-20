# HasData: Search Google Flights

Retrieves Google Flights results from HasData.

```
GET https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-flights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HasData `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-flights?connectionId=$CONNECTION_ID&arrivalId=string&departureId=string&outboundDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arrivalId": "string",
  "departureId": "string",
  "outboundDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hasData/latest/actions/search-google-flights?${params}`, {
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
| `arrivalId` | string | yes | Arrival airport IATA code or location kgmid. |
| `departureId` | string | yes | Departure airport IATA code or location kgmid. |
| `outboundDate` | string | yes | Outbound travel date in YYYY-MM-DD format. |
| `returnDate` | string | no | Return travel date in YYYY-MM-DD format. |
| `type` | string | no | Flight type such as roundTrip or oneWay. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "airports": [
        {}
      ],
      "bestFlights": [
        {}
      ],
      "otherFlights": [
        {}
      ],
      "priceInsights": {},
      "requestMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `airports` | array<object> |  |
| `bestFlights` | array<object> |  |
| `otherFlights` | array<object> |  |
| `priceInsights` | object |  |
| `requestMetadata` | object |  |

## Native endpoint

Through the native HasData API, this operation is `GET /scrape/google/flights` (base URL `https://api.hasdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-flights.md) for the provider-specific parameters and requirements.

