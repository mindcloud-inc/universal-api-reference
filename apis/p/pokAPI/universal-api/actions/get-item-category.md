# PokéAPI: Get Item Category

Retrieves details for an item category from PokéAPI.

```
GET https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PokéAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item-category?connectionId=$CONNECTION_ID&itemCategoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "itemCategoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pokAPI/latest/actions/get-item-category?${params}`, {
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
| `itemCategoryId` | string | yes | Identifier for the requested Item Category record. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "items": [
        {}
      ],
      "name": "Ava Chen",
      "names": [
        {}
      ],
      "pocket": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `items` | array<object> |  |
| `name` | string |  |
| `names` | array<object> |  |
| `pocket` | object |  |

## Native endpoint

Through the native PokéAPI API, this operation is `GET item-category/:itemCategoryId` (base URL `https://pokeapi.co/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-item-category.md) for the provider-specific parameters and requirements.

