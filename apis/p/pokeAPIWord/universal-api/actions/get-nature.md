# PokeAPI Word: Get Nature

Retrieves details for a nature from PokeAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-nature
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokeAPI Word `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-nature?connectionId=$CONNECTION_ID&natureId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "natureId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokeAPIWord/latest/actions/get-nature?${params}`, {
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
| `natureId` | string | yes | Identifier for the requested nature. Use an ID or name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "decreased_stat": {},
      "hates_flavor": {},
      "id": 1,
      "increased_stat": {},
      "likes_flavor": {},
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
| `decreased_stat` | object |  |
| `hates_flavor` | object |  |
| `id` | number |  |
| `increased_stat` | object |  |
| `likes_flavor` | object |  |
| `name` | string |  |
| `names` | array<object> |  |

## Native endpoint

Through the native PokeAPI Word API, this operation is `GET nature/[:natureId]` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nature.md) for the provider-specific parameters and requirements.

