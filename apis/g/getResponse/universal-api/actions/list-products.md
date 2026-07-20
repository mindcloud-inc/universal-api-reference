# GetResponse: List Products

Retrieves products from a GetResponse shop.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0&shopId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/list-products?${params}`, {
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
| `shopId` | string | yes | Shop identifier |
| `name` | string | no | Search products by name |
| `vendor` | string | no | Search products by vendor |
| `category` | string | no | Search products by category name |
| `categoryId` | string | no | Search products by category ID |
| `externalId` | string | no | Search products by external ID |
| `variantName` | string | no | Search products by product variant name |
| `metaFieldNames` | string | no | Comma-separated meta field names to search |
| `metaFieldValues` | string | no | Comma-separated meta field values to search |
| `createdOnFrom` | string | no | Search products created from this date |
| `createdOnTo` | string | no | Search products created to this date |
| `sortName` | string | no | Sort by name |
| `sortCreatedOn` | string | no | Sort by date |
| `fields` | string | no | Comma-separated list of fields to return |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GetResponse API returns.

## Native endpoint

Through the native GetResponse API, this operation is `GET /shops/:shopId/products` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

