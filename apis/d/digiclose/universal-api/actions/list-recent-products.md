# Digiclose: List Recent Products



```
GET https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-recent-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-recent-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/list-recent-products?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Digiclose API, this operation is `GET /products/recent` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-products.md) for the provider-specific parameters and requirements.

