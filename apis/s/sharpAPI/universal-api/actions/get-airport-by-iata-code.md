# SharpAPI: Get Airport By Iata Code

Retrieves an airport by IATA code from SharpAPI.

```
GET https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/get-airport-by-iata-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/get-airport-by-iata-code?connectionId=$CONNECTION_ID&iata=SIN" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iata": "SIN"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/get-airport-by-iata-code?${params}`, {
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
| `iata` | string | yes | IATA airport code. Example: `SIN`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "iata": "string",
      "icao": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Airport city. |
| `country` | string | Airport country code. |
| `iata` | string | IATA airport code. |
| `icao` | string | ICAO airport code. |
| `id` | string | Airport identifier. |
| `name` | string | Airport name. |

## Native endpoint

Through the native SharpAPI API, this operation is `GET /airports/iata/:iata` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-airport-by-iata-code.md) for the provider-specific parameters and requirements.

