# Cogmento CRM: List Products



```
GET https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cogmento CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cogmentoCRM/latest/actions/list-products?${params}`, {
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
      "accountId": "string",
      "acl": [
        {}
      ],
      "category": "string",
      "cost": 1,
      "createdAt": "string",
      "createdBy": {
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "description": "string",
      "id": "string",
      "inventory": 1,
      "lastModified": "string",
      "listPrice": 1,
      "name": "Ava Chen",
      "private": true,
      "rating": 1,
      "salePrice": 1,
      "sku": "string",
      "tags": [
        {}
      ],
      "templateId": "string",
      "wholesalePrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `acl` | array<object> |  |
| `category` | string |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `description` | string |  |
| `id` | string |  |
| `inventory` | number |  |
| `lastModified` | string |  |
| `listPrice` | number |  |
| `name` | string |  |
| `private` | boolean |  |
| `rating` | number |  |
| `salePrice` | number |  |
| `sku` | string |  |
| `tags` | array<object> |  |
| `templateId` | string |  |
| `wholesalePrice` | number |  |

## Native endpoint

Through the native Cogmento CRM API, this operation is `GET /products/` (base URL `https://api.freecrm.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

