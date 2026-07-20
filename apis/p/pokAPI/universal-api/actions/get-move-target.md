# PokéAPI: Get Move Target

Retrieves details for a move target from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-target
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-target?connectionId=$CONNECTION_ID&moveTargetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moveTargetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-target?${params}`, {
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
| `moveTargetId` | string | yes | Identifier for the requested Move Target record. |

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
      "moves": [
        {}
      ],
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
| `descriptions` | array<object> |  |
| `id` | number |  |
| `moves` | array<object> |  |
| `name` | string |  |
| `names` | array<object> |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET move-target/:moveTargetId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-move-target.md) for the provider-specific parameters and requirements.

