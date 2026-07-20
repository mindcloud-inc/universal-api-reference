# PokeAPI Word: Get Pokemon

Retrieves details for a Pokemon from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon?connectionId=$CONNECTION_ID&pokemonId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon?${params}`, {
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
| `pokemonId` | string | yes | Identifier for the requested Pokemon record. Use an ID or name, such as 1 or bulbasaur. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abilities": [
        {}
      ],
      "base_experience": 1,
      "height": 1,
      "id": 1,
      "name": "Ava Chen",
      "sprites": {},
      "types": [
        {}
      ],
      "weight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abilities` | array<object> |  |
| `base_experience` | number |  |
| `height` | number |  |
| `id` | number |  |
| `name` | string |  |
| `sprites` | object |  |
| `types` | array<object> |  |
| `weight` | number |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET pokemon/[:pokemonId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon.md) for the provider-specific parameters and requirements.

