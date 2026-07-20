# Emporix Commerce Engine: Get Product

Retrieves a product from Emporix Commerce Engine.

```
GET https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Emporix Commerce Engine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emporixCommerceEngine/latest/actions/get-product?${params}`, {
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
| `productId` | string | yes | The unique ID of the product. |

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

Through the native Emporix Commerce Engine API, this operation is `GET /product/{{credentials.tenantId}}/products/:productId` (base URL `https://api.emporix.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

