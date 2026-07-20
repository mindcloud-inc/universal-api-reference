# Airlabs: List Aircraft Fleets

Retrieves airline fleet data from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-aircraft-fleets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-aircraft-fleets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-aircraft-fleets?${params}`, {
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
| `airlineIata` | string | no | Filter by airline IATA code. |
| `regNumber` | string | no | Filter by aircraft registration number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "age": "string",
      "airline_iata": "string",
      "airline_icao": "string",
      "alt": 1,
      "built": "string",
      "category": "string",
      "dir": 1,
      "engine": "string",
      "engine_count": "string",
      "flag": "string",
      "hex": "string",
      "iata": "string",
      "icao": "string",
      "last_seen": 1,
      "lat": 1,
      "line": "string",
      "lng": 1,
      "manufacturer": "string",
      "model": "string",
      "msn": "string",
      "reg_number": "string",
      "seen": 1,
      "speed": 1,
      "squawk": "string",
      "type": "string",
      "v_speed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `age` | string | Aircraft age. |
| `airline_iata` | string | Airline IATA code. |
| `airline_icao` | string | Airline ICAO code. |
| `alt` | number | Last altitude. |
| `built` | string | Build year. |
| `category` | string | Aircraft category. |
| `dir` | number | Last direction. |
| `engine` | string | Engine type. |
| `engine_count` | string | Engine count. |
| `flag` | string | Aircraft country code. |
| `hex` | string | ICAO24 hex address. |
| `iata` | string | Aircraft IATA type code. |
| `icao` | string | Aircraft ICAO type code. |
| `last_seen` | number | Last seen timestamp. |
| `lat` | number | Last latitude. |
| `line` | string | Production line number. |
| `lng` | number | Last longitude. |
| `manufacturer` | string | Aircraft manufacturer. |
| `model` | string | Aircraft model. |
| `msn` | string | Manufacturer serial number. |
| `reg_number` | string | Aircraft registration number. |
| `seen` | number | Last seen timestamp. |
| `speed` | number | Last speed. |
| `squawk` | string | Transponder squawk code. |
| `type` | string | Aircraft type. |
| `v_speed` | number | Last vertical speed. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /fleets` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-aircraft-fleets.md) for the provider-specific parameters and requirements.

