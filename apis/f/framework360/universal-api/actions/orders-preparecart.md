# Framework360: Prepare Order



```
POST https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-preparecart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-preparecart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cart[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/orders-preparecart', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cart[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cart[]` | array<object> | yes | Items to add to the cart. |
| `customerId` | number | no | Customer ID for the cart preparation. |
| `shippingId` | number | no | Shipping method ID. |
| `paymentId` | number | no | Payment method ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST orders/prepareCart` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/orders-preparecart.md) for the provider-specific parameters and requirements.

