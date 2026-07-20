# PokeAPI Word: Get Move

Retrieves details for a move from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-move
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-move?connectionId=$CONNECTION_ID&moveId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moveId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-move?${params}`, {
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
| `moveId` | string | yes | Identifier for the requested move. Use an ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accuracy": 1,
      "effect_entries": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "power": 1,
      "pp": 1,
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
| `effect_entries` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `power` | number |  |
| `pp` | number |  |
| `type` | object |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET move/[:moveId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-move.md) for the provider-specific parameters and requirements.

