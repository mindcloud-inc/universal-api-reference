# Emporix Commerce Engine: Search Products

Finds products in Emporix Commerce Engine by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/search-products?${params}`, {
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
      "brandId": "string",
      "categoryIds": [
        "string"
      ],
      "code": "string",
      "description": "string",
      "id": "string",
      "labelIds": [
        "string"
      ],
      "metadata": {},
      "name": "Ava Chen",
      "productType": "string",
      "published": true,
      "template": {},
      "yrn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandId` | string |  |
| `categoryIds` | array<string> |  |
| `code` | string |  |
| `description` | string |  |
| `id` | string |  |
| `labelIds` | array<string> |  |
| `metadata` | object |  |
| `name` | string |  |
| `productType` | string |  |
| `published` | boolean |  |
| `template` | object |  |
| `yrn` | string |  |

## Native endpoint

Through the native Emporix Commerce Engine API, this operation is `POST /product/{{credentials.tenantId}}/products/search` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

