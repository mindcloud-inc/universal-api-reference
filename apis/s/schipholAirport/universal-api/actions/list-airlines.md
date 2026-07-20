# Schiphol Airport: List Airlines

Retrieves a list of airlines from Schiphol Airport.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-airlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-airlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-airlines?${params}`, {
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
| `sort` | string | no | Sort expression using publicName, iata, icao, or nvls. Default: `+iata`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iata": "string",
      "icao": "string",
      "nvls": 1,
      "publicName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iata` | string |  |
| `icao` | string |  |
| `nvls` | number |  |
| `publicName` | string |  |

## Native endpoint

Through the native Schiphol Airport API, this operation is `GET /airlines` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airlines.md) for the provider-specific parameters and requirements.

