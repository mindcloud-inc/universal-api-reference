# Printify: Get Order

Retrieves an order from Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-order?connectionId=$CONNECTION_ID&orderId=69d9645b98c77b61480a2deb&shopId=27141936" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "69d9645b98c77b61480a2deb",
  "shopId": "27141936"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/get-order?${params}`, {
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
| `orderId` | string | yes | Printify order id. Default: `69d9645b98c77b61480a2deb`. |
| `shopId` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appOrderId": "string",
      "createdAt": "string",
      "fulfilmentType": "string",
      "id": "string",
      "shippingMethod": 1,
      "status": "string",
      "totalPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appOrderId` | string |  |
| `createdAt` | string |  |
| `fulfilmentType` | string |  |
| `id` | string |  |
| `shippingMethod` | number |  |
| `status` | string |  |
| `totalPrice` | number |  |

## Native endpoint

Through the native Printify API, this operation is `GET /shops/:shop_id/orders/:order_id.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

