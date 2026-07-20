# PokéAPI: Get Pokemon Shape

Retrieves details for a pokemon shape from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-shape
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-shape?connectionId=$CONNECTION_ID&pokemonShapeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonShapeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-shape?${params}`, {
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
| `pokemonShapeId` | string | yes | Identifier for the requested Pokemon Shape record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "awesome_names": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon_species": [
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
| `awesome_names` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokemon_species` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokemon-shape/:pokemonShapeId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-shape.md) for the provider-specific parameters and requirements.

