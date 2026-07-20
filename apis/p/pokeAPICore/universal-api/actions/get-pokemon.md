# PokeAPI Core: Get Pokemon

Retrieves a Pokemon from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokemon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokemon?connectionId=$CONNECTION_ID&idOrName=ditto" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "ditto"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-pokemon?${params}`, {
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
| `idOrName` | string | yes | Pokemon numeric ID or exact PokeAPI name, such as ditto. Example: `ditto`. |

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
      "forms": [
        {}
      ],
      "height": 1,
      "id": 1,
      "moves": [
        {}
      ],
      "name": "Ava Chen",
      "species": {},
      "sprites": {},
      "stats": [
        {}
      ],
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
| `abilities` | array<object> | Abilities associated with the Pokemon. |
| `base_experience` | number | Base experience value for the Pokemon. |
| `forms` | array<object> | Pokemon form references. |
| `height` | number | Pokemon height in decimetres. |
| `id` | number | Numeric Pokemon identifier. |
| `moves` | array<object> | Move learnset records. |
| `name` | string | Pokemon resource name. |
| `species` | object | Pokemon species reference. |
| `sprites` | object | Sprite image URL set. |
| `stats` | array<object> | Base stat values. |
| `types` | array<object> | Pokemon type slots. |
| `weight` | number | Pokemon weight in hectograms. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /pokemon/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon.md) for the provider-specific parameters and requirements.

