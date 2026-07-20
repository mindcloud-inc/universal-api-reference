# PokéAPI: Get Pokedex

Retrieves details for a pokedex from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokedex
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokedex?connectionId=$CONNECTION_ID&pokedexId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokedexId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokedex?${params}`, {
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
| `pokedexId` | string | yes | Identifier for the requested Pokedex record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "descriptions": [
        {}
      ],
      "id": 1,
      "is_main_series": true,
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon_entries": [
        {}
      ],
      "region": "string",
      "version_groups": [
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
| `descriptions` | array<object> |  |
| `id` | number |  |
| `is_main_series` | boolean |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokemon_entries` | array<object> |  |
| `region` | string |  |
| `version_groups` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokedex/:pokedexId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokedex.md) for the provider-specific parameters and requirements.

