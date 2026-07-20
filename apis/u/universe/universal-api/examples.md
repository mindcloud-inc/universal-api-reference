# Universe Universal API Examples

These examples use the MindCloud API key and Universe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Viewer

Retrieves the authenticated viewer from Universe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-viewer?connectionId=$CONNECTION_ID&query=query%20%7B%20viewer%20%7B%20id%20firstName%20lastName%20memberships%20%7B%20nodes%20%7B%20id%20owner%20%7B%20id%20name%20%7D%20%7D%20%7D%20%7D%20%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query { viewer { id firstName lastName memberships { nodes { id owner { id name } } } } }"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-viewer?${params}`, {
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

See the full [Get Viewer action reference](actions/get-viewer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/universe/latest/actions/get-viewer).

## Check In Order Item

Checks in a specific Universe order item.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/universe/latest/actions/check-in-order-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "mutation CheckInOrderItem($input: OrderItemCheckInInput!) {\n  orderItemCheckIn(input: $input) {\n    errors\n    orderItem {\n      id\n      checkInState\n      state\n      qrCode\n    }\n  }\n}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/universe/latest/actions/check-in-order-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "mutation CheckInOrderItem($input: OrderItemCheckInInput!) {\n  orderItemCheckIn(input: $input) {\n    errors\n    orderItem {\n      id\n      checkInState\n      state\n      qrCode\n    }\n  }\n}"
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
      "checkInState": "string",
      "errors": [
        "string"
      ],
      "id": "string",
      "orderItem": {},
      "orderItemCheckIn": {},
      "qrCode": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Check In Order Item action reference](actions/check-in-order-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/universe/latest/actions/check-in-order-item).
