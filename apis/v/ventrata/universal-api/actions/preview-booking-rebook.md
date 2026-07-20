# Ventrata: Preview Booking Rebook

Previews an existing booking rebook in Ventrata.

```
PUT https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/preview-booking-rebook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/preview-booking-rebook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/preview-booking-rebook', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | Booking UUID from Ventrata. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `availability.id` | string |  |
| `availability.status` | string |  |
| `availability.statusCode` | string |  |
| `availabilityId` | string |  |
| `cancellable` | boolean |  |
| `cancellation.reason` | string |  |
| `cancellation.refund` | string |  |
| `cancellation.utcCancelledAt` | date |  |
| `confirmable` | boolean |  |
| `contact.emailAddress` | string |  |
| `emailReceipt` | boolean |  |
| `id` | string |  |
| `localDateTimeEnd` | date |  |
| `localDateTimeStart` | date |  |
| `notes` | string |  |
| `option.id` | string |  |
| `optionId` | string |  |
| `orderId` | string |  |
| `orderReference` | string |  |
| `product.id` | string |  |
| `product.internalName` | string |  |
| `productId` | string |  |
| `quote` | boolean |  |
| `reseller.id` | string |  |
| `reseller.name` | string |  |
| `resellerReference` | string |  |
| `settlementMethod` | string |  |
| `status` | string |  |
| `supplierReference` | string |  |
| `testMode` | boolean |  |
| `unitItems[].id` | string |  |
| `unitItems[].status` | string |  |
| `unitItems[].unitId` | string |  |
| `unitItems[].unitType` | string |  |
| `unitItems[].uuid` | string |  |
| `updatable` | boolean |  |
| `utcConfirmedAt` | date |  |
| `utcCreatedAt` | date |  |
| `utcExpiresAt` | date |  |
| `utcUpdatedAt` | date |  |
| `uuid` | string |  |
| `voucher.redemptionMethod` | string |  |

## Native endpoint

Through the native Ventrata API, this operation is `POST octo/bookings/:uuid/rebook/preview` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/preview-booking-rebook.md) for the provider-specific parameters and requirements.

