# Ecwid: Get Recently Used Product Swatches

Retrieves recently used product swatches from Ecwid.

```
GET https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-recently-used-product-swatches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-recently-used-product-swatches?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/get-recently-used-product-swatches?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecwid API returns.

## Native endpoint

Through the native Ecwid API, this operation is `GET /:storeId/swatches` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recently-used-product-swatches.md) for the provider-specific parameters and requirements.

