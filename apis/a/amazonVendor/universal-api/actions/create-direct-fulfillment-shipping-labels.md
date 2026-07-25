# Amazon Vendor: Create Direct Fulfillment Shipping Labels



```
POST https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/create-direct-fulfillment-shipping-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/create-direct-fulfillment-shipping-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderNumber": "string",
  "sellingParty": {},
  "shipFromParty": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/create-direct-fulfillment-shipping-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderNumber": "string",
    "sellingParty": {},
    "shipFromParty": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderNumber` | string | yes | Amazon purchase order number for the Direct Fulfillment shipping label request. |
| `sellingParty` | object | yes | Selling party information for the Direct Fulfillment shipping label request. |
| `shipFromParty` | object | yes | Ship-from party information for the Direct Fulfillment shipping label request. |
| `containers[]` | array<object> | no | Container details for the Direct Fulfillment shipping label request. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `POST /vendor/directFulfillment/shipping/2021-12-28/shippingLabels/:purchaseOrderNumber` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-fulfillment-shipping-labels.md) for the provider-specific parameters and requirements.

