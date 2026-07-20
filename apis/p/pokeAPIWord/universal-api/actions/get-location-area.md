# PokeAPI Word: Get Location Area

Retrieves location area details from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-location-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-location-area?connectionId=$CONNECTION_ID&locationAreaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationAreaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-location-area?${params}`, {
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
| `locationAreaId` | string | yes | Identifier for the requested location area. Use an ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "encounter_method_rates": [
        {}
      ],
      "game_index": 1,
      "id": 1,
      "location": {},
      "name": "Ava Chen",
      "pokemon_encounters": [
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
| `encounter_method_rates` | array<object> |  |
| `game_index` | number |  |
| `id` | number |  |
| `location` | object |  |
| `name` | string |  |
| `pokemon_encounters` | array<object> |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET location-area/[:locationAreaId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location-area.md) for the provider-specific parameters and requirements.

