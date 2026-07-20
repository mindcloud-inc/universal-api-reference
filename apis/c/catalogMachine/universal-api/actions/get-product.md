# Catalog Machine: Get Product

Retrieves a product by code from Catalog Machine.

```
GET https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Catalog Machine `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/get-product?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/catalogMachine/latest/actions/get-product?${params}`, {
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
| `code` | string | yes | Unique product code. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product` | object |  |

## Native endpoint

Through the native Catalog Machine API, this operation is `GET /products/:code` (base URL `https://www.catalogmachine.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

