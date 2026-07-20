# PokéAPI: Get Generation

Retrieves details for a generation from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-generation?connectionId=$CONNECTION_ID&generationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-generation?${params}`, {
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
| `generationId` | string | yes | Identifier for the requested Generation record. |

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
| `abilities` | array<object> |  |
| `id` | number |  |
| `main_region` | object |  |
| `moves` | array<object> |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokemon_species` | array<object> |  |
| `types` | array<object> |  |
| `version_groups` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET generation/:generationId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation.md) for the provider-specific parameters and requirements.

