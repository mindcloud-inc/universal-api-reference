# PokeAPI Word: Get Stat

Retrieves details for a stat from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-stat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-stat?connectionId=$CONNECTION_ID&statId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "statId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-stat?${params}`, {
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
| `statId` | string | yes | Identifier for the requested stat. Use an ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affecting_moves": {},
      "affecting_natures": {},
      "characteristics": [
        {}
      ],
      "game_index": 1,
      "id": 1,
      "is_battle_only": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affecting_moves` | object |  |
| `affecting_natures` | object |  |
| `characteristics` | array<object> |  |
| `game_index` | number |  |
| `id` | number |  |
| `is_battle_only` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET stat/[:statId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stat.md) for the provider-specific parameters and requirements.

