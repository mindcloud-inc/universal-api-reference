# Gelato: Cover Dimensions

Retrieves cover dimensions for a Gelato product.

```
GET https://connect.mindcloud.co/v1/universal/gelato/latest/actions/cover-dimensions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gelato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gelato/latest/actions/cover-dimensions?connectionId=$CONNECTION_ID&productUid=string&pageCount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productUid": "string",
  "pageCount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gelato/latest/actions/cover-dimensions?${params}`, {
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
| `productUid` | string | yes |  |
| `pageCount` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gelato API returns.

## Native endpoint

Through the native Gelato API, this operation is `GET https://product.gelatoapis.com/v3/products/{{productUid}}/cover-dimensions` (base URL `https://order.gelatoapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cover-dimensions.md) for the provider-specific parameters and requirements.

