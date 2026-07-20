# Checkout Page: List Subscriptions

Retrieves subscriptions from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-subscriptions?${params}`, {
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
| `search` | string | no | List all subscriptions |
| `pageId` | string | no | Unique identifier. Must be in BSON ObjectId format. |
| `status` | string | no | List all subscriptions |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abandonedCartEmailSentAt": "2026-05-07T12:00:00.000Z",
      "abandonedCartEmailStatus": "ava@example.com",
      "amount": 1,
      "amountUsd": 1,
      "billing": {},
      "cancelAt": "2026-05-07T12:00:00.000Z",
      "cancelAtPeriodEnd": true,
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "canceledBy": "string",
      "couponId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "currentPeriodEnd": "2026-05-07T12:00:00.000Z",
      "currentPeriodStart": "2026-05-07T12:00:00.000Z",
      "customerEmail": "ava@example.com",
      "customerId": "string",
      "discountedFromPrice": 1,
      "dynamicPrice": 1,
      "fees": [
        {}
      ],
      "fields": [
        {}
      ],
      "id": "string",
      "interval": "string",
      "intervalCount": 1,
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
| `amount` | number |  |
| `amountUsd` | number |  |
| `billing` | object |  |
| `cancelAt` | date |  |
| `cancelAtPeriodEnd` | boolean |  |
| `canceledAt` | date |  |
| `canceledBy` | string |  |
| `couponId` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `currentPeriodEnd` | date |  |
| `currentPeriodStart` | date |  |
| `customerEmail` | string |  |
| `customerId` | string |  |
| `discountedFromPrice` | number |  |
| `dynamicPrice` | number |  |
| `fees` | array<object> |  |
| `fields` | array<object> |  |
| `id` | string |  |
| `interval` | string |  |
| `intervalCount` | number |  |
| `isAbandoned` | boolean |  |
| `licenseKeyId` | string |  |
| `pageId` | string |  |
| `productId` | string |  |
| `sellerId` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/subscriptions/` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

