# Schiphol Airport: List Aircraft Types

Retrieves aircraft types from Schiphol Airport.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-aircraft-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-aircraft-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/list-aircraft-types?${params}`, {
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
| `iataMain` | string | no | Three-character IATA main aircraft type code. |
| `iataSub` | string | no | Three-character IATA sub aircraft type code. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Result page number, starting at 0. Default: `0`. |
| `sort` | string | no | Sort expression using iataMain, iataSub, longDescription, or shortDescription. Default: `+iataMain`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iataMain": "string",
      "iataSub": "string",
      "longDescription": "string",
      "shortDescription": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iataMain` | string |  |
| `iataSub` | string |  |
| `longDescription` | string |  |
| `shortDescription` | string |  |

## Native endpoint

Through the native Schiphol Airport API, this operation is `GET /aircrafttypes` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-aircraft-types.md) for the provider-specific parameters and requirements.

