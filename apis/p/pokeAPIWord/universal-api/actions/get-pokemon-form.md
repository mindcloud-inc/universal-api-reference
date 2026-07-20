# PokeAPI Word: Get Pokemon Form

Retrieves Pokemon form details from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon-form?connectionId=$CONNECTION_ID&pokemonFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-pokemon-form?${params}`, {
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
| `pokemonFormId` | string | yes | Identifier for the requested Pokemon form. Use an ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form_order": 1,
      "id": 1,
      "is_default": true,
      "name": "Ava Chen",
      "order": 1,
      "pokemon": {},
      "types": [
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
| `form_order` | number |  |
| `id` | number |  |
| `is_default` | boolean |  |
| `name` | string |  |
| `order` | number |  |
| `pokemon` | object |  |
| `types` | array<object> |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET pokemon-form/[:pokemonFormId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-form.md) for the provider-specific parameters and requirements.

