# PokeAPI Core: Get Region

Retrieves a region from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-region?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-region?${params}`, {
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
| `idOrName` | string | yes | Region numeric ID or exact PokeAPI region name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "locations": [
        {}
      ],
      "main_generation": {},
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokedexes": [
        {}
      ],
      "version_groups": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Numeric region identifier. |
| `locations` | array<object> | Locations in this region. |
| `main_generation` | object | Main generation reference. |
| `name` | string | Region resource name. |
| `names` | array<object> | Localized region names. |
| `pokedexes` | array<object> | Pokedexes associated with this region. |
| `version_groups` | array<object> | Version groups associated with this region. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /region/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-region.md) for the provider-specific parameters and requirements.

