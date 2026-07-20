# SquareSpace: Get Products

Retrieves products from Squarespace by ID.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-products?connectionId=$CONNECTION_ID&ids=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "ids": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-products?${params}`, {
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
| `ids` | string | yes | Product IDs (comma-separated). |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `products` | array<object> |  |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /v2/commerce/products/:ids` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-products.md) for the provider-specific parameters and requirements.

