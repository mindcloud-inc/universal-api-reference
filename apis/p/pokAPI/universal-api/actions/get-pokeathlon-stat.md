# PokéAPI: Get Pokeathlon Stat

Retrieves details for a pokeathlon stat from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokeathlon-stat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokeathlon-stat?connectionId=$CONNECTION_ID&pokeathlonStatId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pokeathlonStatId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-pokeathlon-stat?${params}`, {
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
| `pokeathlonStatId` | string | yes | Identifier for the requested Pokeathlon Stat record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affecting_natures": {},
      "id": 1,
      "name": "Ava Chen",
      "names": [
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
| `affecting_natures` | object |  |
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET pokeathlon-stat/:pokeathlonStatId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pokeathlon-stat.md) for the provider-specific parameters and requirements.

