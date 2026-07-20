# Revi.io Reviews: Get Product Review Info

Retrieves product review info from Revi.io Reviews.

```
GET https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-product-review-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revi.io Reviews `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-product-review-info?connectionId=$CONNECTION_ID&idProduct=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "idProduct": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/get-product-review-info?${params}`, {
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
| `idProduct` | string | yes | The product ID to inspect. |
| `idStore` | string | no | Marketplace store ID when querying marketplace data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Envelope containing the returned product rating object. |
| `success` | boolean | Whether the product review info request succeeded. |

## Native endpoint

Through the native Revi.io Reviews API, this operation is `GET /product_info` (base URL `https://api.revi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product-review-info.md) for the provider-specific parameters and requirements.

