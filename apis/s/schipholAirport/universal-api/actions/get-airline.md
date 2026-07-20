# Schiphol Airport: Get Airline

Retrieves an airline from Schiphol Airport by IATA or ICAO code.

```
GET https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-airline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Schiphol Airport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-airline?connectionId=$CONNECTION_ID&airline=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "airline": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/schipholAirport/latest/actions/get-airline?${params}`, {
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
| `airline` | string | yes | IATA or ICAO airline code, such as KL or KLM. |

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

Through the native Schiphol Airport API, this operation is `GET /airlines/:airline` (base URL `https://api.schiphol.nl/public-flights`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-airline.md) for the provider-specific parameters and requirements.

