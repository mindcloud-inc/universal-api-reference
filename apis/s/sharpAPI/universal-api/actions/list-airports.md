# SharpAPI: List Airports

Retrieves airports from SharpAPI.

```
GET https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/list-airports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SharpAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/list-airports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sharpAPI/latest/actions/list-airports?${params}`, {
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
| `page` | number | no | Page number to retrieve. Example: `1`. |
| `perPage` | number | no | Number of airports to return per page. Example: `3`. |

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

Through the native SharpAPI API, this operation is `GET /airports` (base URL `https://sharpapi.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-airports.md) for the provider-specific parameters and requirements.

