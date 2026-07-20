# PokéAPI: Get API Resources

Retrieves PokéAPI resource endpoints.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-api-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-api-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-api-resources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "ability": "string",
      "berry": "string",
      "berry-firmness": "string",
      "berry-flavor": "string",
      "characteristic": "string",
      "contest-effect": "string",
      "contest-type": "string",
      "egg-group": "string",
      "encounter-condition": "string",
      "encounter-condition-value": "string",
      "encounter-method": "string",
      "evolution-chain": "string",
      "evolution-trigger": "string",
      "gender": "string",
      "generation": "string",
      "growth-rate": "string",
      "item": "string",
      "item-attribute": "string",
      "item-category": "string",
      "item-fling-effect": "string",
      "item-pocket": "string",
      "language": "string",
      "location": "string",
      "location-area": "string",
      "machine": "string",
      "meta": "string",
      "move": "string",
      "move-ailment": "string",
      "move-battle-style": "string",
      "move-category": "string",
      "move-damage-class": "string",
      "move-learn-method": "string",
      "move-target": "string",
      "nature": "string",
      "pal-park-area": "string",
      "pokeathlon-stat": "string",
      "pokedex": "string",
      "pokemon": "string",
      "pokemon-color": "string",
      "pokemon-form": "string",
      "pokemon-habitat": "string",
      "pokemon-shape": "string",
      "pokemon-species": "string",
      "region": "string",
      "stat": "string",
      "super-contest-effect": "string",
      "type": "string",
      "version": "string",
      "version-group": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ability` | string |  |
| `berry` | string |  |
| `berry-firmness` | string |  |
| `berry-flavor` | string |  |
| `characteristic` | string |  |
| `contest-effect` | string |  |
| `contest-type` | string |  |
| `egg-group` | string |  |
| `encounter-condition` | string |  |
| `encounter-condition-value` | string |  |
| `encounter-method` | string |  |
| `evolution-chain` | string |  |
| `evolution-trigger` | string |  |
| `gender` | string |  |
| `generation` | string |  |
| `growth-rate` | string |  |
| `item` | string |  |
| `item-attribute` | string |  |
| `item-category` | string |  |
| `item-fling-effect` | string |  |
| `item-pocket` | string |  |
| `language` | string |  |
| `location` | string |  |
| `location-area` | string |  |
| `machine` | string |  |
| `meta` | string |  |
| `move` | string |  |
| `move-ailment` | string |  |
| `move-battle-style` | string |  |
| `move-category` | string |  |
| `move-damage-class` | string |  |
| `move-learn-method` | string |  |
| `move-target` | string |  |
| `nature` | string |  |
| `pal-park-area` | string |  |
| `pokeathlon-stat` | string |  |
| `pokedex` | string |  |
| `pokemon` | string |  |
| `pokemon-color` | string |  |
| `pokemon-form` | string |  |
| `pokemon-habitat` | string |  |
| `pokemon-shape` | string |  |
| `pokemon-species` | string |  |
| `region` | string |  |
| `stat` | string |  |
| `super-contest-effect` | string |  |
| `type` | string |  |
| `version` | string |  |
| `version-group` | string |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET /` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-resources.md) for the provider-specific parameters and requirements.

