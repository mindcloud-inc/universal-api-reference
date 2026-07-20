# Digiclose: Create Product



```
POST https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digiclose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "name": "Ava Chen",
  "price": 1,
  "shortDescription": "string",
  "vat": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digiclose/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "name": "Ava Chen",
    "price": 1,
    "shortDescription": "string",
    "vat": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes |  |
| `name` | string | yes |  |
| `price` | number | yes |  |
| `shortDescription` | string | yes |  |
| `vat` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "productId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `productId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Digiclose API, this operation is `POST /products` (base URL `https://app.digiclose.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

