# Spoonacular Food: Search Grocery Product by UPC

Finds a grocery product in Spoonacular Food by UPC.

```
GET https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-grocery-product-by-upc
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoonacular Food `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-grocery-product-by-upc?connectionId=$CONNECTION_ID&upc=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "upc": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-grocery-product-by-upc?${params}`, {
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
| `upc` | string | yes | The product UPC code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "image": "string",
      "title": "string",
      "upc": "string"
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
| `title` | string |  |
| `upc` | string |  |

## Native endpoint

Through the native Spoonacular Food API, this operation is `GET /food/products/upc/:upc` (base URL `https://api.spoonacular.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-grocery-product-by-upc.md) for the provider-specific parameters and requirements.

