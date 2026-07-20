# PokeAPI Core: Get Location

Retrieves a location from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-location?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-location?${params}`, {
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
| `idOrName` | string | yes | Location numeric ID or exact PokeAPI location name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "areas": [
        {}
      ],
      "game_indices": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "region": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `areas` | array<object> | Areas within this location. |
| `game_indices` | array<object> | Game index records. |
| `id` | number | Numeric location identifier. |
| `name` | string | Location resource name. |
| `names` | array<object> | Localized location names. |
| `region` | object | Region reference. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /location/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

