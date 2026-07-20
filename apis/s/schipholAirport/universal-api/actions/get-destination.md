# Schiphol Airport: Get Destination

Retrieves a destination from Schiphol Airport by IATA code.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-destination?connectionId=$CONNECTION_ID&iata=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iata": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-destination?${params}`, {
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
| `iata` | string | yes | Three-character destination IATA code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "iata": "string",
      "publicName": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `iata` | string |  |
| `publicName` | object |  |

## Native endpoint

Through the native Schiphol Airport API, this operation is `GET /destinations/:iata` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-destination.md) for the provider-specific parameters and requirements.

