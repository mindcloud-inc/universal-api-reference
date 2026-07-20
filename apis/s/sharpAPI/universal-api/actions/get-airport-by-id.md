# SharpAPI: Get Airport By Id

Retrieves an airport from SharpAPI.

```
GET https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/get-airport-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/get-airport-by-id?connectionId=$CONNECTION_ID&id=1ef266e0-00ca-656e-b481-06bb2780ed98" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1ef266e0-00ca-656e-b481-06bb2780ed98"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/get-airport-by-id?${params}`, {
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
| `id` | string | yes | Airport identifier. Example: `1ef266e0-00ca-656e-b481-06bb2780ed98`. |

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

Through the native SharpAPI API, this operation is `GET /airports/:id` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-airport-by-id.md) for the provider-specific parameters and requirements.

