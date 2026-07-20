# Airlabs: List Airports

Retrieves airport database records from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-airports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-airports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-airports?${params}`, {
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
| `countryCode` | string | no | Filter by country ISO 2 code. |
| `iataCode` | string | no | Filter by airport IATA code. |
| `icaoCode` | string | no | Filter by airport ICAO code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "iata_code": "string",
      "icao_code": "string",
      "lat": 1,
      "lng": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string | Country ISO 2 code. |
| `iata_code` | string | Airport IATA code. |
| `icao_code` | string | Airport ICAO code. |
| `lat` | number | Airport latitude. |
| `lng` | number | Airport longitude. |
| `name` | string | Airport name. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /airports` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airports.md) for the provider-specific parameters and requirements.

