# Botbaba: Create Product



```
POST https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "productName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "productName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | Bot identifier. |
| `productName` | string | yes | Product name. |
| `description` | string | no | Product description. |
| `sku` | string | no | Stock keeping unit. |
| `price` | number | no | Product price. |
| `displayPrice` | number | no | Display price. |
| `displayDiscountPer` | number | no | Display discount percentage. |
| `type` | string | no | Product type. |
| `image` | string | no | Image payload or URL. |
| `imageExtension` | string | no | Image file extension. |
| `foodType` | string | no | Food type. |
| `isSpicy` | boolean | no | Whether the product is spicy. |
| `isActive` | boolean | no | Whether the product is active. |
| `categories[]` | array<number> | no | Category identifiers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native Botbaba API, this operation is `POST /api/InsertProduct` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

