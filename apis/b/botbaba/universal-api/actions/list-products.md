# Botbaba: List Products



```
GET https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Botbaba `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/list-products?connectionId=$CONNECTION_ID&botId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "botId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/list-products?${params}`, {
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
| `botId` | number | yes | The Botbaba bot identifier. |
| `page` | number | no | Optional result page number. |
| `pageSize` | number | no | Optional page size. |
| `searchKey` | string | no | Optional search text for products. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": 1,
      "botName": "Ava Chen",
      "categories": [
        1
      ],
      "description": "string",
      "displayDiscountPer": 1,
      "displayPrice": 1,
      "foodType": "string",
      "id": 1,
      "image": "string",
      "isActive": true,
      "isSpicy": true,
      "price": 1,
      "productName": "Ava Chen",
      "sku": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | number |  |
| `botName` | string |  |
| `categories` | array<number> |  |
| `description` | string |  |
| `displayDiscountPer` | number |  |
| `displayPrice` | number |  |
| `foodType` | string |  |
| `id` | number |  |
| `image` | string |  |
| `isActive` | boolean |  |
| `isSpicy` | boolean |  |
| `price` | number |  |
| `productName` | string |  |
| `sku` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Botbaba API, this operation is `GET /api/GetProducts` (base URL `https://app.botbaba.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.

