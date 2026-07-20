# Printify: Calculate Order Shipping

Calculates order shipping in Printify.

```
GET https://connect.mindcloud.co/v1/universal/printify/latest/actions/calculate-order-shipping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Printify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/printify/latest/actions/calculate-order-shipping?connectionId=$CONNECTION_ID&address_to=%5Bobject%20Object%5D&line_items=%5Bobject%20Object%5D&shop_id=27141936" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address_to": "[object Object]",
  "line_items": "[object Object]",
  "shop_id": "27141936"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/printify/latest/actions/calculate-order-shipping?${params}`, {
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
| `address_to` | object | yes | Recipient address for shipping calculation. |
| `line_items` | list<object> | yes | Order line items for shipping calculation. |
| `shop_id` | number | yes | Printify shop id. Default: `27141936`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "economy": 1,
      "express": 1,
      "printifyExpress": 1,
      "priority": 1,
      "standard": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `economy` | number |  |
| `express` | number |  |
| `printifyExpress` | number |  |
| `priority` | number |  |
| `standard` | number |  |

## Native endpoint

Through the native Printify API, this operation is `POST /shops/:shop_id/orders/shipping.json` (base URL `https://api.printify.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-order-shipping.md) for the provider-specific parameters and requirements.

