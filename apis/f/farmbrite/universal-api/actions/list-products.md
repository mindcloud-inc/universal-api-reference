# Farmbrite: List products

Retrieves a list of products from Farmbrite.

```
GET https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Farmbrite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/farmbrite/latest/actions/list-products?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `sortBy` | string | no |  |
| `sortDir` | list | no | One of: `Ascending`, `Descending`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "currentPage": 1,
      "data": [
        {
          "availableOnline": true,
          "cartId": "string",
          "category": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "deliveryOptions": [
            "string"
          ],
          "description": "string",
          "electronicId": "string",
          "id": "string",
          "increment": 1,
          "isParent": true,
          "minOrder": "string",
          "parentProductId": "string",
          "pinned": true,
          "price": 1,
          "qtyRemaining": "string",
          "sku": "string",
          "status": "string",
          "taxBehavior": "string",
          "taxCode": "string",
          "taxRate": "string",
          "title": "string",
          "transactionCategoryId": "string",
          "type": "string",
          "unitLabel": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "wholesaleOnly": true,
          "wholesalePrice": "string"
        }
      ],
      "limit": 1,
      "message": "string",
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cached` | boolean |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `data[].availableOnline` | boolean |  |
| `data[].cartId` | string |  |
| `data[].category` | string |  |
| `data[].createdAt` | date |  |
| `data[].deliveryOptions` | array<string> |  |
| `data[].description` | string |  |
| `data[].electronicId` | string |  |
| `data[].id` | string |  |
| `data[].increment` | number |  |
| `data[].isParent` | boolean |  |
| `data[].minOrder` | string |  |
| `data[].parentProductId` | string |  |
| `data[].pinned` | boolean |  |
| `data[].price` | number |  |
| `data[].qtyRemaining` | string |  |
| `data[].sku` | string |  |
| `data[].status` | string |  |
| `data[].taxBehavior` | string |  |
| `data[].taxCode` | string |  |
| `data[].taxRate` | string |  |
| `data[].title` | string |  |
| `data[].transactionCategoryId` | string |  |
| `data[].type` | string |  |
| `data[].unitLabel` | string |  |
| `data[].updatedAt` | date |  |
| `data[].wholesaleOnly` | boolean |  |
| `data[].wholesalePrice` | string |  |
| `limit` | number |  |
| `message` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Farmbrite API, this operation is `GET /products` (base URL `https://api.farmbrite.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

