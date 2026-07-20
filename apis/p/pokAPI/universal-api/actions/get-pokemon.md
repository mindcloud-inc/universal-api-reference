# PokéAPI: Get Pokemon

Retrieves details for a pokemon from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon?connectionId=$CONNECTION_ID&pId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon?${params}`, {
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
| `pId` | string | yes | Identifier for the requested Pokemon record. |

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
      "cries": {},
      "forms": [
        {}
      ],
      "game_indices": [
        {}
      ],
      "height": 1,
      "held_items": [
        {}
      ],
      "id": 1,
      "is_default": true,
      "location_area_encounters": "string",
      "moves": [
        {}
      ],
      "name": "Ava Chen",
      "order": 1,
      "past_abilities": [
        {}
      ],
      "past_stats": [
        {}
      ],
      "past_types": [
        {}
      ],
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
| `abilities` | array<object> |  |
| `base_experience` | number |  |
| `cries` | object |  |
| `forms` | array<object> |  |
| `game_indices` | array<object> |  |
| `height` | number |  |
| `held_items` | array<object> |  |
| `id` | number |  |
| `is_default` | boolean |  |
| `location_area_encounters` | string |  |
| `moves` | array<object> |  |
| `name` | string |  |
| `order` | number |  |
| `past_abilities` | array<object> |  |
| `past_stats` | array<object> |  |
| `past_types` | array<object> |  |
| `species` | object |  |
| `sprites` | object |  |
| `stats` | array<object> |  |
| `types` | array<object> |  |
| `weight` | number |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokemon/:pId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon.md) for the provider-specific parameters and requirements.

