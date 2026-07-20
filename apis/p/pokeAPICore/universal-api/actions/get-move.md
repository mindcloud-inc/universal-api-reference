# PokeAPI Core: Get Move

Retrieves a move from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-move
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-move?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-move?${params}`, {
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
| `idOrName` | string | yes | Move numeric ID or exact PokeAPI move name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": 1,
      "damage_class": {},
      "effect_entries": [
        {}
      ],
      "generation": {},
      "id": 1,
      "learned_by_pokemon": [
        {}
      ],
      "name": "Ava Chen",
      "power": 1,
      "pp": 1,
      "priority": 1,
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accuracy` | number | Move accuracy, when provided. |
| `damage_class` | object | Damage class reference. |
| `effect_entries` | array<object> | Localized effect text entries. |
| `generation` | object | Generation reference. |
| `id` | number | Numeric move identifier. |
| `learned_by_pokemon` | array<object> | Pokemon that can learn the move. |
| `name` | string | Move resource name. |
| `power` | number | Move power, when provided. |
| `pp` | number | Move PP value. |
| `priority` | number | Move priority value. |
| `type` | object | Move type reference. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /move/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-move.md) for the provider-specific parameters and requirements.

