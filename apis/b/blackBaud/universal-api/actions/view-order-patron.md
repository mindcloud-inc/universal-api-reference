# BlackBaud: View Order Patron



```
GET https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/view-order-patron
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlackBaud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/view-order-patron?connectionId=$CONNECTION_ID&salesOrderId=Sales%20order%20ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "salesOrderId": "Sales order ID"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blackBaud/latest/actions/view-order-patron?${params}`, {
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
| `salesOrderId` | string | yes | The Blackbaud sales order identifier. Example: `Sales order ID`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BlackBaud API returns.

## Native endpoint

Through the native BlackBaud API, this operation is `GET alt-slsmg/orders/{sales_order_id}/view` (base URL `https://api.sky.blackbaud.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-order-patron.md) for the provider-specific parameters and requirements.

