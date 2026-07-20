# Zoho Billing: Retrieve Product



```
GET https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-product?connectionId=$CONNECTION_ID&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/retrieve-product?${params}`, {
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
| `productId` | string | yes | Unique identifier of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "product": {
        "autonumber_enabled": true,
        "created_at": "2026-05-07T12:00:00.000Z",
        "created_time": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "items_associated": [
          [
            {}
          ]
        ],
        "name": "Ava Chen",
        "next_number": "string",
        "prefix_string": "string",
        "product_digest": "string",
        "product_id": "string",
        "status": "string",
        "updated_time": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `product` | object |  |
| `product.autonumber_enabled` | boolean |  |
| `product.created_at` | date |  |
| `product.created_time` | date |  |
| `product.description` | string |  |
| `product.items_associated[]` | array<object> |  |
| `product.name` | string |  |
| `product.next_number` | string |  |
| `product.prefix_string` | string |  |
| `product.product_digest` | string |  |
| `product.product_id` | string |  |
| `product.status` | string |  |
| `product.updated_time` | date |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `GET /products/:product_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product.md) for the provider-specific parameters and requirements.

