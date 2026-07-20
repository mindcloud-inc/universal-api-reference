# Schiphol Airport: List Destinations

Retrieves a list of destinations from Schiphol Airport.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-destinations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-destinations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-destinations?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Result page number, starting at 0. Default: `0`. |
| `sort` | string | no | Sort expression using publicName.dutch, publicName.english, iata, country, or city. Default: `+iata`. |

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

Through the native Schiphol Airport API, this operation is `GET /destinations` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-destinations.md) for the provider-specific parameters and requirements.

