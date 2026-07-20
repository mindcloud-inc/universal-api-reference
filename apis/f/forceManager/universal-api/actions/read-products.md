# ForceManager: Read Products

Retrieves products from your ForceManager account.

```
GET https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ForceManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/forceManager/latest/actions/read-products?${params}`, {
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
      "categoryId": 1,
      "description": "string",
      "extId": "string",
      "id": 1,
      "model": "string",
      "notAvailable": true,
      "price": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryId` | number | ID of the category of the product. |
| `description` | string | Comment for the product. |
| `extId` | string | External id of the product from a third-party system. |
| `id` | number | Unique identifier for the product. |
| `model` | string | Name of the product. |
| `notAvailable` | boolean | Whether the product is not available. |
| `price` | number | Selling price for the product. |

## Native endpoint

Through the native ForceManager API, this operation is `GET /products`. The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-products.md) for the provider-specific parameters and requirements.

