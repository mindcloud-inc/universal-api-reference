# PokeAPI Word: Get Evolution Trigger

Retrieves evolution trigger details from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-evolution-trigger
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-evolution-trigger?connectionId=$CONNECTION_ID&evolutionTriggerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "evolutionTriggerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-evolution-trigger?${params}`, {
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
| `evolutionTriggerId` | string | yes | Identifier for the requested evolution trigger. Use an ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon_species": [
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
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokemon_species` | array<object> |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET evolution-trigger/[:evolutionTriggerId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-evolution-trigger.md) for the provider-specific parameters and requirements.

