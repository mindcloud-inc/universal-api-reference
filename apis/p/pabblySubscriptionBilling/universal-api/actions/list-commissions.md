# Pabbly Subscription Billing: List Commissions



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-commissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-commissions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-commissions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateEmail": "ava@example.com",
      "affiliateId": "string",
      "clickId": "string",
      "commissionAmount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customerEmail": "ava@example.com",
      "id": "string",
      "invoiceId": "string",
      "invoiceNumber": "string",
      "isPaid": "string",
      "isVoid": true,
      "payoutDate": "string",
      "planId": "string",
      "productName": "Ava Chen",
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
| `affiliateEmail` | string |  |
| `affiliateId` | string |  |
| `clickId` | string |  |
| `commissionAmount` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customerEmail` | string |  |
| `id` | string |  |
| `invoiceId` | string |  |
| `invoiceNumber` | string |  |
| `isPaid` | string |  |
| `isVoid` | boolean |  |
| `payoutDate` | string |  |
| `planId` | string |  |
| `productName` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/commissions` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-commissions.md) for the provider-specific parameters and requirements.

