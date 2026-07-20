# Emporix Commerce Engine: List Products

Retrieves products from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/list-products?${params}`, {
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

Through the native Emporix Commerce Engine API, this operation is `GET /product/{{credentials.tenantId}}/products` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

