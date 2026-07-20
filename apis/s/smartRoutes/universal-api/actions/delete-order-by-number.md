# SmartRoutes: Delete Order By Number



```
DELETE https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/delete-order-by-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/delete-order-by-number?connectionId=$CONNECTION_ID&orderNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/delete-order-by-number?${params}`, {
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
| `orderNumber` | string | yes | Order number of the order to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lineItemsCount": 1,
      "ordersCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lineItemsCount` | number | Number of order line items deleted by the request. |
| `ordersCount` | number | Number of orders deleted by the request. |

## Native endpoint

Through the native SmartRoutes API, this operation is `DELETE /orders/order-number/:order_number` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-order-by-number.md) for the provider-specific parameters and requirements.

