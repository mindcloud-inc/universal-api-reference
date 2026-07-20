# PokéAPI: Get Type

Retrieves details for a type from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-type?connectionId=$CONNECTION_ID&typeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "typeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-type?${params}`, {
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
| `typeId` | string | yes | Identifier for the requested Type record. |

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
      "names": [
        {}
      ],
      "past_damage_relations": [
        {}
      ],
      "pokemon": [
        {}
      ],
      "sprites": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `damage_relations` | object |  |
| `game_indices` | array<object> |  |
| `generation` | object |  |
| `id` | number |  |
| `move_damage_class` | object |  |
| `moves` | array<object> |  |
| `name` | string |  |
| `names` | array<object> |  |
| `past_damage_relations` | array<object> |  |
| `pokemon` | array<object> |  |
| `sprites` | object |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET type/:typeId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-type.md) for the provider-specific parameters and requirements.

