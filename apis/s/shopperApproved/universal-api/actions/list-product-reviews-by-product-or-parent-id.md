# Shopper Approved: List Product Reviews by Product or Parent ID

Retrieves product reviews from Shopper Approved by product ID.

```
GET https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-product-reviews-by-product-or-parent-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-product-reviews-by-product-or-parent-id?connectionId=$CONNECTION_ID&limit=25&offset=0&productId=SKU-100" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "productId": "SKU-100"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-product-reviews-by-product-or-parent-id?${params}`, {
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
| `productId` | string | yes | The product ID or parent ID. Example: `SKU-100`. |
| `from` | date | no | The first date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `to` | date | no | The last date in YYYY-MM-DD format. Example: `2026-03-24`. |
| `sort` | string | no | How the reviews should be sorted. Example: `newest`. |
| `removed` | number | no | Whether to include removed reviews. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopper Approved API returns.

## Native endpoint

Through the native Shopper Approved API, this operation is `GET /products/reviews/:siteid/:productid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-product-reviews-by-product-or-parent-id.md) for the provider-specific parameters and requirements.

