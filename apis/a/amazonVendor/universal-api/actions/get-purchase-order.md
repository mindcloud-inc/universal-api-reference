# Amazon Vendor: Get Purchase Order



```
GET https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Vendor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-purchase-order?connectionId=$CONNECTION_ID&purchaseOrderNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonVendor/latest/actions/get-purchase-order?${params}`, {
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
| `purchaseOrderNumber` | string | yes | The 8-character alphanumeric purchase order identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Amazon Vendor API returns.

## Native endpoint

Through the native Amazon Vendor API, this operation is `GET /vendor/orders/v1/purchaseOrders/:purchaseOrderNumber` (base URL `https://sellingpartnerapi-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order.md) for the provider-specific parameters and requirements.

