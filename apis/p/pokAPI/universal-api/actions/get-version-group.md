# PokéAPI: Get Version Group

Retrieves details for a version group from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-version-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-version-group?connectionId=$CONNECTION_ID&versionGroupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "versionGroupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-version-group?${params}`, {
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
| `versionGroupId` | string | yes | Identifier for the requested Version Group record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generation": {},
      "id": 1,
      "move_learn_methods": [
        {}
      ],
      "name": "Ava Chen",
      "order": 1,
      "pokedexes": [
        {}
      ],
      "regions": [
        {}
      ],
      "versions": [
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
| `generation` | object |  |
| `id` | number |  |
| `move_learn_methods` | array<object> |  |
| `name` | string |  |
| `order` | number |  |
| `pokedexes` | array<object> |  |
| `regions` | array<object> |  |
| `versions` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET version-group/:versionGroupId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-version-group.md) for the provider-specific parameters and requirements.

