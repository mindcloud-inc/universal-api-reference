# Omnisend: Get Product

Retrieves a product from Omnisend.

```
GET https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/get-product?connectionId=$CONNECTION_ID&productID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/get-product?${params}`, {
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
| `productID` | string | yes | Unique Omnisend product identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `GET /v5/products/:productID` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

