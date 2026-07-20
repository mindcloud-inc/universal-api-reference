# Ventrata Universal API Examples

These examples use the MindCloud API key and Ventrata connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Capabilities

Retrieves capabilities from Ventrata.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-capabilities?${params}`, {
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
      "dependencies": [
        "string"
      ],
      "docs": "string",
      "id": "string",
      "required": true,
      "revision": 1
    }
  ],
  "meta": {}
}
```

See the full [List Capabilities action reference](actions/list-capabilities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ventrata/latest/actions/list-capabilities).

## Confirm Booking

Confirms an existing booking in Ventrata.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/confirm-booking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/confirm-booking', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string"
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
      "active": true,
      "availability": {
        "id": "string",
        "status": "string",
        "statusCode": "string"
      },
      "availabilityId": "string",
      "cancellable": true,
      "cancellation": {
        "reason": "string",
        "refund": "string",
        "utcCancelledAt": "2026-05-07T12:00:00.000Z"
      },
      "confirmable": true,
      "contact": {
        "emailAddress": "ava@example.com"
      },
      "emailReceipt": true,
      "id": "string",
      "localDateTimeEnd": "2026-05-07T12:00:00.000Z",
      "localDateTimeStart": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "option": {
        "id": "string"
      },
      "optionId": "string",
      "orderId": "string",
      "orderReference": "string",
      "product": {
        "id": "string",
        "internalName": "Ava Chen"
      },
      "productId": "string",
      "quote": true,
      "reseller": {
        "id": "string",
        "name": "Ava Chen"
      },
      "resellerReference": "string",
      "settlementMethod": "string",
      "status": "string",
      "supplierReference": "string",
      "testMode": true,
      "unitItems": [
        {
          "id": "string",
          "status": "string",
          "unitId": "string",
          "unitType": "string",
          "uuid": "string"
        }
      ],
      "updatable": true,
      "utcConfirmedAt": "2026-05-07T12:00:00.000Z",
      "utcCreatedAt": "2026-05-07T12:00:00.000Z",
      "utcExpiresAt": "2026-05-07T12:00:00.000Z",
      "utcUpdatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "voucher": {
        "redemptionMethod": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Confirm Booking action reference](actions/confirm-booking.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ventrata/latest/actions/confirm-booking).
