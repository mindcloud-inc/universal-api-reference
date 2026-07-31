# SWAPI: Get Starship



```
GET https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-starship
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-starship?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWAPI/latest/actions/get-starship?${params}`, {
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
| `id` | number | yes | The numeric starship identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost_in_credits": "string",
      "crew": "string",
      "length": "string",
      "manufacturer": "string",
      "model": "string",
      "name": "Ava Chen",
      "passengers": "string",
      "starship_class": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost_in_credits` | string |  |
| `crew` | string |  |
| `length` | string |  |
| `manufacturer` | string |  |
| `model` | string |  |
| `name` | string |  |
| `passengers` | string |  |
| `starship_class` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SWAPI API, this operation is `GET /starships/:id/` (base URL `https://swapi.dev/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-starship.md) for the provider-specific parameters and requirements.

