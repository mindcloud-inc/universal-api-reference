# Digiclose: Get Product



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-product?connectionId=$CONNECTION_ID&productId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "productId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/get-product?${params}`, {
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
| `productId` | number | yes | Unique identifier for the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "price": 1,
      "shortDescription": "string",
      "totalPrice": 1,
      "updatedAt": "string",
      "uuid": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `price` | number |  |
| `shortDescription` | string |  |
| `totalPrice` | number |  |
| `updatedAt` | string |  |
| `uuid` | string |  |
| `vat` | number |  |

## Native endpoint

Through the native Digiclose API, this operation is `GET /products/:product_id` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.

