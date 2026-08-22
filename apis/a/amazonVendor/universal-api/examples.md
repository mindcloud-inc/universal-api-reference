# Amazon Vendor Universal API Examples

These examples use the MindCloud API key and Amazon Vendor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Direct Fulfillment Packing Slip



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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Get Direct Fulfillment Packing Slip action reference](actions/get-direct-fulfillment-packing-slip.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amazonVendor/latest/actions/get-direct-fulfillment-packing-slip).

## Create Direct Fulfillment Shipping Labels



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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Direct Fulfillment Shipping Labels action reference](actions/create-direct-fulfillment-shipping-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amazonVendor/latest/actions/create-direct-fulfillment-shipping-labels).
