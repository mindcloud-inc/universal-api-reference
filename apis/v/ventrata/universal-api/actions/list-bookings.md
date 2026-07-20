# Ventrata: List Bookings

Retrieves bookings from Ventrata.

```
GET https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ventrata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-bookings?connectionId=$CONNECTION_ID&optionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "optionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ventrata/latest/actions/list-bookings?${params}`, {
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
| `resellerReference` | string | no | Primary filter by reseller booking reference. |
| `supplierReference` | string | no | Primary filter by supplier booking reference. |
| `localDate` | string | no | Primary filter by booking local date (YYYY-MM-DD). |
| `localDateStart` | string | no | Primary filter start date; must be paired with localDateEnd. |
| `localDateEnd` | string | no | Primary filter end date; must be paired with localDateStart. |
| `availabilityId` | string | no | Primary filter by availability identifier. |
| `utcCreatedAtStart` | string | no | Primary filter start timestamp; must be paired with utcCreatedAtEnd. |
| `utcCreatedAtEnd` | string | no | Primary filter end timestamp; must be paired with utcCreatedAtStart. |
| `utcUpdatedAtStart` | string | no | Primary filter start timestamp; must be paired with utcUpdatedAtEnd. |
| `utcUpdatedAtEnd` | string | no | Primary filter end timestamp; must be paired with utcUpdatedAtStart. |
| `utcRedeemedAtStart` | string | no | Primary filter start timestamp; must be paired with utcRedeemedAtEnd. |
| `utcRedeemedAtEnd` | string | no | Primary filter end timestamp; must be paired with utcRedeemedAtStart. |
| `utcNoshowedAtStart` | string | no | Primary filter start timestamp; must be paired with utcNoshowedAtEnd. |
| `utcNoshowedAtEnd` | string | no | Primary filter end timestamp; must be paired with utcNoshowedAtStart. |
| `utcRebookedAtStart` | string | no | Primary filter start timestamp; must be paired with utcRebookedAtEnd. |
| `utcRebookedAtEnd` | string | no | Primary filter end timestamp; must be paired with utcRebookedAtStart. |
| `utcCancelledAtStart` | string | no | Primary filter start timestamp; must be paired with utcCancelledAtEnd. |
| `utcCancelledAtEnd` | string | no | Primary filter end timestamp; must be paired with utcCancelledAtStart. |
| `contactEmailAddress` | string | no | Primary filter by contact email address. |
| `contactPhoneNumber` | string | no | Primary filter by contact phone number. |
| `contactLastName` | string | no | Primary filter by contact last name. Must be at least 3 characters. |
| `status` | string | no | Optional booking status filter. |
| `tag` | string | no | Optional filter by booking tag. |
| `productId` | string | no | Optional filter by product identifier. |
| `optionId` | string | yes | Option filter. Use DEFAULT for the default option. |
| `page` | number | no | Optional page number. |
| `perPage` | number | no | Optional page size. |

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

Through the native Ventrata API, this operation is `GET octo/bookings` (base URL `https://api.ventrata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

