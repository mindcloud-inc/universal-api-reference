# MailBluster: List Products

Retrieves a page of products from MailBluster.

```
GET https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/list-products?${params}`, {
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
| `pageNo` | number | no | Page number to retrieve. Default: `1`. |
| `perPage` | number | no | Number of products to retrieve per page. Default: `10`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "nextPageNo": 1,
        "pageNo": 1,
        "perPage": 1,
        "prevPageNo": 1,
        "total": 1,
        "totalPage": 1
      },
      "products": [
        {
          "createdAt": "string",
          "id": "string",
          "name": "Ava Chen",
          "updatedAt": "string"
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
| `meta` | object | Pagination metadata. |
| `meta.nextPageNo` | number | Next page number when available. |
| `meta.pageNo` | number | Current page number. |
| `meta.perPage` | number | Products per page. |
| `meta.prevPageNo` | number | Previous page number when available. |
| `meta.total` | number | Total number of products. |
| `meta.totalPage` | number | Total number of pages. |
| `products` | array<object> | Products in the requested page. |
| `products[].createdAt` | string | Creation timestamp. |
| `products[].id` | string | Product ID. |
| `products[].name` | string | Product name. |
| `products[].updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native MailBluster API, this operation is `GET /products` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

