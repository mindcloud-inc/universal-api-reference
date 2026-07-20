# PokeAPI Core: Get Type

Retrieves a type from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-type?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-type?${params}`, {
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
| `idOrName` | string | yes | Type numeric ID or exact PokeAPI type name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "damage_relations": {},
      "game_indices": [
        {}
      ],
      "generation": {},
      "id": 1,
      "move_damage_class": {},
      "moves": [
        {}
      ],
      "name": "Ava Chen",
      "pokemon": [
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
| `damage_relations` | object | Damage relationship groups for this type. |
| `game_indices` | array<object> | Game index records. |
| `generation` | object | Generation reference. |
| `id` | number | Numeric type identifier. |
| `move_damage_class` | object | Move damage class reference. |
| `moves` | array<object> | Moves with this type. |
| `name` | string | Type resource name. |
| `pokemon` | array<object> | Pokemon with this type. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /type/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-type.md) for the provider-specific parameters and requirements.

