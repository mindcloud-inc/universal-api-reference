# Swell: Update Product



```
PUT https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swell/latest/actions/update-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Swell product ID. |
| `name` | string | no | The product name. |
| `price` | number | no | The product price. |
| `active` | boolean | no | Whether the product is active. |
| `options[]` | array<object> | no | Product option definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "delivery": "string",
      "id": "string",
      "name": "Ava Chen",
      "price": 1,
      "slug": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `delivery` | string |  |
| `id` | string |  |
| `name` | string |  |
| `price` | number |  |
| `slug` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Swell API, this operation is `PUT /products/:id` (base URL `https://api.swell.store`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.

