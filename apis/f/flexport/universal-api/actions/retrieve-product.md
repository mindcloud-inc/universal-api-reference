# Flexport: Retrieve Product

Retrieves a product from your Flexport account.

```
GET https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-product?connectionId=$CONNECTION_ID&id=prod_12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "prod_12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexport/latest/actions/retrieve-product?${params}`, {
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
| `id` | string | yes | Unique Flexport product ID to retrieve. Example: `prod_12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "classifications": [
        {}
      ],
      "clientVerified": true,
      "countryOfOrigin": "string",
      "description": "string",
      "hsCodes": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "productCategory": "string",
      "productProperties": [
        {}
      ],
      "sku": "string",
      "suppliers": [
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
| `archivedAt` | date |  |
| `classifications` | array<object> |  |
| `clientVerified` | boolean |  |
| `countryOfOrigin` | string |  |
| `description` | string |  |
| `hsCodes` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `productCategory` | string |  |
| `productProperties` | array<object> |  |
| `sku` | string |  |
| `suppliers` | array<object> |  |

## Native endpoint

Through the native Flexport API, this operation is `GET /products/:id` (base URL `https://api.flexport.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-product.md) for the provider-specific parameters and requirements.

