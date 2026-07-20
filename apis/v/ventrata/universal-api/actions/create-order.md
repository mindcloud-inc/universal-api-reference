# Ventrata: Create Order

Creates a new order in Ventrata.

```
POST https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/create-order', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "bookings": [
        {
          "id": "string",
          "orderId": "string",
          "orderReference": "string",
          "productId": "string",
          "status": "string",
          "uuid": "string"
        }
      ],
      "cancellable": true,
      "confirmable": true,
      "contact": {
        "emailAddress": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "lastName": "Chen"
      },
      "emailReceipt": true,
      "id": "string",
      "invoicePdfUrl": "https://example.com",
      "quote": true,
      "settlementMethod": "string",
      "settlementMethods": [
        "string"
      ],
      "status": "string",
      "supplierReference": "string",
      "testMode": true,
      "updatable": true,
      "utcConfirmedAt": "2026-05-07T12:00:00.000Z",
      "utcCreatedAt": "2026-05-07T12:00:00.000Z",
      "utcExpiresAt": "2026-05-07T12:00:00.000Z",
      "utcUpdatedAt": "2026-05-07T12:00:00.000Z",
      "voucher": {
        "redemptionMethod": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `bookings` | array<object> |  |
| `bookings[].id` | string |  |
| `bookings[].orderId` | string |  |
| `bookings[].orderReference` | string |  |
| `bookings[].productId` | string |  |
| `bookings[].status` | string |  |
| `bookings[].uuid` | string |  |
| `cancellable` | boolean |  |
| `confirmable` | boolean |  |
| `contact.emailAddress` | string |  |
| `contact.firstName` | string |  |
| `contact.fullName` | string |  |
| `contact.lastName` | string |  |
| `emailReceipt` | boolean |  |
| `id` | string |  |
| `invoicePdfUrl` | string |  |
| `quote` | boolean |  |
| `settlementMethod` | string |  |
| `settlementMethods` | array<string> |  |
| `status` | string |  |
| `supplierReference` | string |  |
| `testMode` | boolean |  |
| `updatable` | boolean |  |
| `utcConfirmedAt` | date |  |
| `utcCreatedAt` | date |  |
| `utcExpiresAt` | date |  |
| `utcUpdatedAt` | date |  |
| `voucher.redemptionMethod` | string |  |

## Native endpoint

Through the native Ventrata API, this operation is `POST octo/orders` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

