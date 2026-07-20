# Ventrata: List Orders

Retrieves orders from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-orders?${params}`, {
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
| `supplierReference` | string | no | Filter by exact supplier order reference. |
| `utcCreatedAtStart` | string | no | Filter start timestamp; must be paired with utcCreatedAtEnd. |
| `utcCreatedAtEnd` | string | no | Filter end timestamp; must be paired with utcCreatedAtStart. |
| `utcUpdatedAtStart` | string | no | Filter start timestamp; must be paired with utcUpdatedAtEnd. |
| `utcUpdatedAtEnd` | string | no | Filter end timestamp; must be paired with utcUpdatedAtStart. |
| `contactEmailAddress` | string | no | Filter by contact email address. |
| `contactPhoneNumber` | string | no | Filter by contact phone number. |
| `contactLastName` | string | no | Filter by contact last name. |

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

Through the native Ventrata API, this operation is `GET octo/orders` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

