# PokeAPI Word: Get Pokemon Species

Retrieves Pokemon species details from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon-species
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon-species?connectionId=$CONNECTION_ID&pokemonSpeciesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonSpeciesId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon-species?${params}`, {
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
| `pokemonSpeciesId` | string | yes | Identifier for the requested Pokemon species. Use an ID or name, such as 1 or bulbasaur. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base_happiness": 1,
      "capture_rate": 1,
      "color": {},
      "evolution_chain": {},
      "flavor_text_entries": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base_happiness` | number |  |
| `capture_rate` | number |  |
| `color` | object |  |
| `evolution_chain` | object |  |
| `flavor_text_entries` | array<object> |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET pokemon-species/[:pokemonSpeciesId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-species.md) for the provider-specific parameters and requirements.

