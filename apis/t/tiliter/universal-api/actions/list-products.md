# Tiliter: List Products

Retrieves products from the Tiliter Recognition API.

```
GET https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tiliter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tiliter/latest/actions/list-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "products": [
        {
          "archetypeId": "string",
          "department": "string",
          "optionalAttributes": [
            "string"
          ],
          "productDescription": "string",
          "productId": "string",
          "productName": "Ava Chen",
          "recognitionEnabled": true,
          "requiredAttributes": [
            "string"
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `products` | array<object> |  |
| `products[].archetypeId` | string |  |
| `products[].department` | string |  |
| `products[].optionalAttributes` | array |  |
| `products[].productDescription` | string |  |
| `products[].productId` | string |  |
| `products[].productName` | string |  |
| `products[].recognitionEnabled` | boolean |  |
| `products[].requiredAttributes` | array |  |

## Native endpoint

Through the native Tiliter API, this operation is `GET /products/` (base URL `https://recognition.services.tiliter.com/v1/15`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

