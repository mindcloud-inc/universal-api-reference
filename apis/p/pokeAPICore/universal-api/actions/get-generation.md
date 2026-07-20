# PokeAPI Core: Get Generation

Retrieves a generation from PokeAPI Core.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-generation?connectionId=$CONNECTION_ID&idOrName=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idOrName": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPICore/latest/actions/get-generation?${params}`, {
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
| `idOrName` | string | yes | Generation numeric ID or exact PokeAPI generation name. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abilities": [
        {}
      ],
      "id": 1,
      "main_region": {},
      "moves": [
        {}
      ],
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokemon_species": [
        {}
      ],
      "types": [
        {}
      ],
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
| `abilities` | array<object> | Abilities introduced in this generation. |
| `id` | number | Numeric generation identifier. |
| `main_region` | object | Main region reference. |
| `moves` | array<object> | Moves introduced in this generation. |
| `name` | string | Generation resource name. |
| `names` | array<object> | Localized generation names. |
| `pokemon_species` | array<object> | Pokemon species introduced in this generation. |
| `types` | array<object> | Types introduced in this generation. |
| `version_groups` | array<object> | Version groups in this generation. |

## Native endpoint

Through the native PokeAPI Core API, this operation is `GET /generation/[:idOrName]/` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation.md) for the provider-specific parameters and requirements.

