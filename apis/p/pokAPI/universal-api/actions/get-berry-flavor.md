# PokéAPI: Get Berry Flavor

Retrieves details for a berry flavor from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-berry-flavor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-berry-flavor?connectionId=$CONNECTION_ID&berryFlavorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "berryFlavorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-berry-flavor?${params}`, {
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
| `berryFlavorId` | string | yes | Identifier for the requested Berry Flavor record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "berries": [
        {}
      ],
      "contest_type": {},
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
| `berries` | array<object> |  |
| `contest_type` | object |  |
| `id` | number |  |
| `name` | string |  |
| `names` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET berry-flavor/:berryFlavorId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-berry-flavor.md) for the provider-specific parameters and requirements.

