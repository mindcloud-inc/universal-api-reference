# Goodbarber eCommerce: Get Order Shipping



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-order-shipping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-order-shipping?connectionId=$CONNECTION_ID&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/get-order-shipping?${params}`, {
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
| `orderId` | number | yes | Unique ID of the order. Default: `1`. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shipping_tracking_num": "string",
      "shipping_tracking_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipping_tracking_num` | string | <div class="field_description">ID that the customer can use to follow the delivery of its order on the carrier website.</div> |
| `shipping_tracking_url` | string | <div class="field_description">URL on which the customer can follow the delivery of its order.</div> |
| `status` | string |  |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/orders/:webzine_id/order/:order_id/shipping/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-shipping.md) for the provider-specific parameters and requirements.

