# Shipday Universal API Examples

These examples use the MindCloud API key and Shipday connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Active Orders

Retrieves active orders from Shipday.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/list-active-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipday/latest/actions/list-active-orders?${params}`, {
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
      "activityLog": {
        "expectedDeliveryDate": "2026-05-07T12:00:00.000Z",
        "expectedDeliveryTime": "2026-05-07T12:00:00.000Z",
        "expectedPickupTime": "2026-05-07T12:00:00.000Z",
        "placementTime": "2026-05-07T12:00:00.000Z"
      },
      "costing": {
        "cashTip": 1,
        "deliveryFee": 1,
        "discountAmount": 1,
        "tax": 1,
        "tip": 1,
        "totalCost": 1
      },
      "customer": {
        "address": "string",
        "emailAddress": "ava@example.com",
        "id": 1,
        "latitude": 1,
        "longitude": 1,
        "name": "Ava Chen",
        "phoneNumber": "string"
      },
      "deliveryInstruction": "string",
      "distance": 1,
      "etaTime": "string",
      "idRequired": true,
      "orderId": 1,
      "orderItems": [
        {
          "detail": "string",
          "name": "Ava Chen",
          "quantity": 1,
          "unitPrice": 1
        }
      ],
      "orderNumber": "string",
      "orderSeqNum": 1,
      "orderStatus": {
        "accepted": true,
        "incomplete": true,
        "orderState": "string"
      },
      "orderStatusAdmin": "string",
      "parentId": 1,
      "pickupInstruction": "string",
      "restaurant": {
        "address": "string",
        "id": 1,
        "latitude": 1,
        "longitude": 1,
        "name": "Ava Chen",
        "phoneNumber": "string"
      },
      "schedule": true,
      "thirdPartyAssignedAnytime": true,
      "trackingLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Active Orders action reference](actions/list-active-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipday/latest/actions/list-active-orders).

## Add Carrier

Creates a new carrier in Shipday.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipday/latest/actions/add-carrier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipday/latest/actions/add-carrier', {
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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Carrier action reference](actions/add-carrier.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shipday/latest/actions/add-carrier).
