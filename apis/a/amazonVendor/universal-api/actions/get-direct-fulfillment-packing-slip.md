# Amazon Vendor: Get Direct Fulfillment Packing Slip



```
GET https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-packing-slip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-packing-slip?connectionId=$CONNECTION_ID&purchaseOrderNumber=e.g.%20UvgABdBjQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderNumber": "e.g. UvgABdBjQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-direct-fulfillment-packing-slip?${params}`, {
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
| `purchaseOrderNumber` | string | yes | The purchaseOrderNumber for the packing slip that you want. Example: `e.g. UvgABdBjQ`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `GET /vendor/directFulfillment/shipping/2021-12-28/packingSlips/:purchaseOrderNumber` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-direct-fulfillment-packing-slip.md) for the provider-specific parameters and requirements.

