# SquareSpace: List Products

Retrieves products from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/list-products?${params}`, {
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
| `modifiedAfter` | date | no | Return products modified after this datetime. |
| `modifiedBefore` | date | no | Return products modified before this datetime. |
| `type` | list<string> | no | Filter products by type. One of: `DIGITAL`, `GIFT_CARD`, `PHYSICAL`, `SERVICE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "products": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination` | object | Pagination metadata. |
| `products` | array<object> | Product rows. |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /v2/commerce/products` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

