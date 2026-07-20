# i2i Universal API Examples

These examples use the MindCloud API key and i2i connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List ship orders

Retrieves ship orders from i2i by status and date range.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/i2i/latest/actions/list-ship-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/i2i/latest/actions/list-ship-orders?${params}`, {
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
      "created": "string",
      "header": {
        "active": "string",
        "cancelled": "2026-05-07T12:00:00.000Z",
        "comment1": "string",
        "comment2": "string",
        "created": "2026-05-07T12:00:00.000Z",
        "id": 1,
        "number": "string",
        "opened": "2026-05-07T12:00:00.000Z",
        "packed": "2026-05-07T12:00:00.000Z",
        "picked": "2026-05-07T12:00:00.000Z",
        "poNo": "string",
        "refNo": "string",
        "service": "string",
        "shipped": "2026-05-07T12:00:00.000Z",
        "shipper": "string",
        "shipto": {
          "address1": "string",
          "address2": "string",
          "city": "Ava Chen",
          "code": "string",
          "contact": "Ava Chen",
          "country": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "postal": "string",
          "province": "string"
        },
        "soldto": {
          "address1": "string",
          "address2": "string",
          "city": "Ava Chen",
          "code": "string",
          "contact": "Ava Chen",
          "country": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "postal": "string",
          "province": "string"
        },
        "status": "string",
        "trackingNo": "string"
      },
      "id": 1,
      "lines": [
        {
          "description": "string",
          "item": "string",
          "orderedLot": "string",
          "orderedQty": 1,
          "pickedQty": 1,
          "picks": [
            {
              "pickedFrom": "string",
              "pickedLot": "string",
              "pickedQty": 1
            }
          ],
          "sentQty": 1
        }
      ],
      "number": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List ship orders action reference](actions/list-ship-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/i2i/latest/actions/list-ship-orders).

## Create order

Creates a new ship order in i2i.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/i2i/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "header": {},
  "lines[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/i2i/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "header": {},
    "lines[]": [{}]
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

See the full [Create order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/i2i/latest/actions/create-order).
