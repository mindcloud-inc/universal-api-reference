# PokéAPI: Get Move Category

Retrieves details for a move category from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-category?connectionId=$CONNECTION_ID&moveCategoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moveCategoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-move-category?${params}`, {
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
| `moveCategoryId` | string | yes | Identifier for the requested Move Category record. |

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
      "name": "Ava Chen"
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

## Native endpoint

Through the native PokéAPI API, this operation is `GET move-category/:moveCategoryId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-move-category.md) for the provider-specific parameters and requirements.

