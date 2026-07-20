# PokéAPI: Get Pokemon Form

Retrieves details for a pokemon form from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-form?connectionId=$CONNECTION_ID&pokemonFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokemonFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokemon-form?${params}`, {
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
| `pokemonFormId` | string | yes | Identifier for the requested Pokemon Form record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "form_name": "Ava Chen",
      "form_names": [
        {}
      ],
      "form_order": 1,
      "id": 1,
      "is_battle_only": true,
      "is_default": true,
      "is_mega": true,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "order": 1,
      "pokemon": {},
      "sprites": {},
      "types": [
        {}
      ],
      "version_group": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `form_name` | string |  |
| `form_names` | array<object> |  |
| `form_order` | number |  |
| `id` | number |  |
| `is_battle_only` | boolean |  |
| `is_default` | boolean |  |
| `is_mega` | boolean |  |
| `name` | string |  |
| `names` | array<object> |  |
| `order` | number |  |
| `pokemon` | object |  |
| `sprites` | object |  |
| `types` | array<object> |  |
| `version_group` | object |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokemon-form/:pokemonFormId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokemon-form.md) for the provider-specific parameters and requirements.

