# Spoonacular Food: Search Grocery Products

Finds grocery products in Spoonacular Food by keyword.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-grocery-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-grocery-products?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-grocery-products?${params}`, {
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
| `query` | string | yes | Grocery product search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "imageType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `image` | string |  |
| `imageType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/products/search` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-grocery-products.md) for the provider-specific parameters and requirements.

