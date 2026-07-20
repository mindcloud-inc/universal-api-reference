# PokeAPI Core: Get Pokedex

Retrieves a Pokedex from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokedex
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokedex?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokedex?${params}`, {
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
| `idOrName` | string | yes | Pokedex numeric ID or exact PokeAPI pokedex name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "descriptions": [
        {}
      ],
      "id": 1,
      "is_main_series": true,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon_entries": [
        {}
      ],
      "region": {},
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
| `descriptions` | array<object> | Localized pokedex descriptions. |
| `id` | number | Numeric pokedex identifier. |
| `is_main_series` | boolean | Whether this pokedex belongs to the main series. |
| `name` | string | Pokedex resource name. |
| `names` | array<object> | Localized pokedex names. |
| `pokemon_entries` | array<object> | Pokemon entries in this pokedex. |
| `region` | object | Region reference, when available. |
| `version_groups` | array<object> | Version groups associated with this pokedex. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /pokedex/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokedex.md) for the provider-specific parameters and requirements.

