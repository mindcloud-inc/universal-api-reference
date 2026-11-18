# Brightpearl Universal API Examples

These examples use the MindCloud API key and Brightpearl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/list-orders?${params}`, {
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
      "contactId": 1,
      "createdById": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customerRef": "string",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "departmentId": 1,
      "externalRef": "string",
      "installedIntegrationInstanceId": 1,
      "orderId": 1,
      "orderPaymentStatusId": 1,
      "orderShippingStatusId": 1,
      "orderStatusId": 1,
      "orderStockStatusId": 1,
      "orderTypeId": 1,
      "parentOrderId": 1,
      "staffOwnerContactId": 1,
      "taxDate": "2026-05-07T12:00:00.000Z",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "warehouseId": 1
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brightpearl/latest/actions/list-orders).

## Add Goods-Out Note Events



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/add-goods-out-note-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "goodsOutNoteId": 1,
  "events[]": [
    {}
  ],
  "events[].eventCode": "PAC",
  "events[].occured": "2026-05-07T12:00:00.000Z",
  "events[].eventOwnerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brightpearl/latest/actions/add-goods-out-note-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "goodsOutNoteId": 1,
    "events[]": [{}],
    "events[].eventCode": "PAC",
    "events[].occured": "2026-05-07T12:00:00.000Z",
    "events[].eventOwnerId": 1
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

See the full [Add Goods-Out Note Events action reference](actions/add-goods-out-note-events.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/brightpearl/latest/actions/add-goods-out-note-events).
