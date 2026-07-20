# Airlabs: List Airlines

Retrieves airline database records from Airlabs.

```
GET https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-airlines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-airlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/list-airlines?${params}`, {
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
| `iataCode` | string | no | Filter by airline IATA code. |
| `icaoCode` | string | no | Filter by airline ICAO code. |
| `name` | string | no | Filter by airline name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "iata_code": "string",
      "icao_code": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `iata_code` | string | Airline IATA code. |
| `icao_code` | string | Airline ICAO code. |
| `name` | string | Airline name. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /airlines` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airlines.md) for the provider-specific parameters and requirements.

