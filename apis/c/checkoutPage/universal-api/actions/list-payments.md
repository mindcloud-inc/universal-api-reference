# Checkout Page: List Payments

Retrieves payments from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-payments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-payments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-payments?${params}`, {
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
| `limit` | string | no | The number of results per page. Minimum value is 1 and maximum is 100. Defaults to 20. |
| `startingAfter` | string | no | A cursor value specifying the id of a resource to start before. Retrieves items that appear after this cursor in the list. Cannot be used together with `ending_before`. |
| `endingBefore` | string | no | A cursor value specifying the id of a resource to end after. Retrieves items that appear before this cursor in the list. Cannot be used together with `starting_after`. |
| `search` | string | no | Case-insensitive search matched against `customerEmail` and `orderId`. Returns documents where either field contains the search term. |
| `status` | string | no | List all payments |
| `pageId` | string | no | Unique identifier. Must be in BSON ObjectId format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abandonedCartEmailSentAt": "2026-05-07T12:00:00.000Z",
      "abandonedCartEmailStatus": "ava@example.com",
      "amount": 1,
      "amountDue": 1,
      "amountExcludingTax": 1,
      "amountPaid": 1,
      "amountUsd": 1,
      "billing": {},
      "canceledAt": "string",
      "canceledBy": "string",
      "canceledReason": "string",
      "coupon": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customerEmail": "ava@example.com",
      "customerId": "string",
      "discount": {},
      "discountedFromPrice": 1,
      "dynamicPrice": 1,
      "fees": [
        {}
      ],
      "fields": [
        {}
      ],
      "id": "string",
      "invoiceId": "string",
      "isAbandoned": true,
      "licenseKeyId": "string",
      "pageId": "string",
      "productId": "string",
      "sellerId": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abandonedCartEmailSentAt` | date |  |
| `abandonedCartEmailStatus` | string |  |
| `amount` | number | The total amount intended to be collected. |
| `amountDue` | number | The outstanding amount of money to be paid. |
| `amountExcludingTax` | number |  |
| `amountPaid` | number | The amount of money paid toward the total. |
| `amountUsd` | number |  |
| `billing` | object |  |
| `canceledAt` | string | The date this was canceled. |
| `canceledBy` | string | The userId that canceled this. If this is a booking, tickets were canceled in addition. |
| `canceledReason` | string | The reason for the cancellation |
| `coupon` | object |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customerEmail` | string |  |
| `customerId` | string |  |
| `discount` | object |  |
| `discountedFromPrice` | number |  |
| `dynamicPrice` | number |  |
| `fees` | array<object> |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `invoiceId` | string |  |
| `isAbandoned` | boolean |  |
| `licenseKeyId` | string |  |
| `pageId` | string |  |
| `productId` | string |  |
| `sellerId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/payments/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payments.md) for the provider-specific parameters and requirements.

