# Extensiv Order Manager Universal API Examples

These examples use the MindCloud API key and Extensiv Order Manager connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders

Retrieves orders from Extensiv Order Manager.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/list-orders?${params}`, {
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
  "data": [
    {
      "orderDate": "2026-05-07T12:00:00.000Z",
      "orderId": 1,
      "orderNumber": "string",
      "orderTotal": {},
      "salesChannelId": 1,
      "status": "string",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/extensiv/latest/actions/list-orders).

## Create External Shipment

Creates an external shipment in Extensiv Order Manager.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-external-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipments[].shipMethod.shippingCarrier": "string",
  "shipments[].trackingNumber": "string",
  "shipments[].shipMethod": {},
  "shipments[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/extensiv/latest/actions/create-external-shipment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipments[].shipMethod.shippingCarrier": "string",
    "shipments[].trackingNumber": "string",
    "shipments[].shipMethod": {},
    "shipments[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "order": {},
      "orderBatchNumber": 1,
      "processingMessage": "string",
      "shipment": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create External Shipment action reference](actions/create-external-shipment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/extensiv/latest/actions/create-external-shipment).
