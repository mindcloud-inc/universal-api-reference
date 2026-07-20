# Shopper Approved: Get Product Aggregate Statistics by Product ID

Retrieves product aggregate statistics from Shopper Approved by product ID.

```
GET https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-product-aggregate-statistics-by-product-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-product-aggregate-statistics-by-product-id?connectionId=$CONNECTION_ID&productId=1001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-product-aggregate-statistics-by-product-id?${params}`, {
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
| `productId` | number | yes | The product ID or parent ID. Example: `1001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopper Approved API returns.

## Native endpoint

Through the native Shopper Approved API, this operation is `GET /aggregates/products/:siteid/:productid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-aggregate-statistics-by-product-id.md) for the provider-specific parameters and requirements.

