# PokéAPI: Get Move

Retrieves details for a move from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move?connectionId=$CONNECTION_ID&moveId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moveId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move?${params}`, {
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
| `moveId` | string | yes | Identifier for the requested Move record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": 1,
      "contest_combos": {},
      "contest_effect": {},
      "contest_type": {},
      "damage_class": {},
      "effect_chance": "string",
      "effect_changes": [
        {}
      ],
      "effect_entries": [
        {}
      ],
      "flavor_text_entries": [
        {}
      ],
      "generation": {},
      "id": 1,
      "learned_by_pokemon": [
        {}
      ],
      "machines": [
        {}
      ],
      "meta": {},
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "past_values": [
        {}
      ],
      "power": 1,
      "pp": 1,
      "priority": 1,
      "stat_changes": [
        {}
      ],
      "super_contest_effect": {},
      "target": {},
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accuracy` | number |  |
| `contest_combos` | object |  |
| `contest_effect` | object |  |
| `contest_type` | object |  |
| `damage_class` | object |  |
| `effect_chance` | string |  |
| `effect_changes` | array<object> |  |
| `effect_entries` | array<object> |  |
| `flavor_text_entries` | array<object> |  |
| `generation` | object |  |
| `id` | number |  |
| `learned_by_pokemon` | array<object> |  |
| `machines` | array<object> |  |
| `meta` | object |  |
| `name` | string |  |
| `names` | array<object> |  |
| `past_values` | array<object> |  |
| `power` | number |  |
| `pp` | number |  |
| `priority` | number |  |
| `stat_changes` | array<object> |  |
| `super_contest_effect` | object |  |
| `target` | object |  |
| `type` | object |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET move/:moveId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-move.md) for the provider-specific parameters and requirements.

