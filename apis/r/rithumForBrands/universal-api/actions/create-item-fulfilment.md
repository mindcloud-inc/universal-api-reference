# Rithum for Brands: Create Item Fulfilment

Create Item fullfilment

```
POST https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-item-fulfilment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-item-fulfilment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/create-item-fulfilment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryStatus` | string | no |  |
| `trackingNumber` | string | no |  |
| `distributionCenterID` | number | no |  |
| `insuranceCost` | number | no |  |
| `orderID` | number | no |  |
| `profileID` | list<number> | no |  |
| `returnTrackingNumber` | string | no |  |
| `sellerFulfillmentID` | string | no |  |
| `serialShippingContainerCode` | string | no |  |
| `shippedDateUtc` | string | no |  |
| `shippingCarrier` | string | no |  |
| `shippingClass` | string | no |  |
| `shippingCost` | number | no |  |
| `shippingLabelRequestID` | string | no |  |
| `stagingLocation` | string | no |  |
| `taxCost` | number | no |  |
| `trackingUrl` | string | no |  |
| `type` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rithum for Brands API returns.

## Native endpoint

Through the native Rithum for Brands API, this operation is `POST Fulfillments` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-item-fulfilment.md) for the provider-specific parameters and requirements.

