# Ecwid: Search Product Brands

Finds product brands in Ecwid.

```
GET https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-product-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-product-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/search-product-brands?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecwid API returns.

## Native endpoint

Through the native Ecwid API, this operation is `GET /:storeId/brands` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-product-brands.md) for the provider-specific parameters and requirements.

