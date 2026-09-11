# Peplink: List All Products



```
GET https://connect.mindcloud.co/v1/universal/peplink/latest/actions/list-all-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peplink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peplink/latest/actions/list-all-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peplink/latest/actions/list-all-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Peplink API returns.

## Native endpoint

Through the native Peplink API, this operation is `GET partner/partner-store-products` (base URL `https://portal.peplink.com/api/e/v1/cp/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-products.md) for the provider-specific parameters and requirements.

