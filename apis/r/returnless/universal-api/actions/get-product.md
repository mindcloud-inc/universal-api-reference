# Returnless: Get Product

Retrieves a product from Returnless.

```
GET https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Returnless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-product?connectionId=$CONNECTION_ID&product=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "product": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-product?${params}`, {
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
| `product` | string | yes | The unique identifier of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Product payload retrieved by ID. |
| `meta` | object | Execution metadata. |

## Native endpoint

Through the native Returnless API, this operation is `GET /2025-01/products/{product}` (base URL `https://api-v2.returnless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

