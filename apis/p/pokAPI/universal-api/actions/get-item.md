# PokéAPI: Get Item

Retrieves details for an item from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item?connectionId=$CONNECTION_ID&itemId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item?${params}`, {
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
| `itemId` | string | yes | Identifier for the requested Item record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": [
        {}
      ],
      "baby_trigger_for": "string",
      "category": {},
      "cost": 1,
      "effect_entries": [
        {}
      ],
      "flavor_text_entries": [
        {}
      ],
      "fling_effect": "string",
      "fling_power": "string",
      "game_indices": [
        {}
      ],
      "held_by_pokemon": [
        {}
      ],
      "id": 1,
      "machines": [
        {}
      ],
      "name": "Ava Chen",
      "names": [
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
| `attributes` | array<object> |  |
| `baby_trigger_for` | string |  |
| `category` | object |  |
| `cost` | number |  |
| `effect_entries` | array<object> |  |
| `flavor_text_entries` | array<object> |  |
| `fling_effect` | string |  |
| `fling_power` | string |  |
| `game_indices` | array<object> |  |
| `held_by_pokemon` | array<object> |  |
| `id` | number |  |
| `machines` | array<object> |  |
| `name` | string |  |
| `names` | array<object> |  |
| `sprites` | object |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET item/:itemId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item.md) for the provider-specific parameters and requirements.

