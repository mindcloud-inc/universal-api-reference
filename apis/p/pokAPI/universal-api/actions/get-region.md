# PokéAPI: Get Region

Retrieves details for a region from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-region?connectionId=$CONNECTION_ID&regionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "regionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-region?${params}`, {
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
| `regionId` | string | yes | Identifier for the requested Region record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "locations": [
        {}
      ],
      "main_generation": {},
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pokedexes": [
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
| `id` | number |  |
| `locations` | array<object> |  |
| `main_generation` | object |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pokedexes` | array<object> |  |
| `version_groups` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET region/:regionId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-region.md) for the provider-specific parameters and requirements.

