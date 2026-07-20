# GoAffPro: List Pending Payouts

Retrieves pending affiliate payouts from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-pending-payouts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-pending-payouts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-pending-payouts?${params}`, {
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
| `affiliateId` | string | no | Only return pending payout amounts for this affiliate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "amount": 1,
      "amountAfterTax": 1,
      "amounts": {
        "mlmReward": 1,
        "paid": 1,
        "salesCommission": 1
      },
      "email": "ava@example.com",
      "name": "Ava Chen",
      "paidOut": 1,
      "pending": 1,
      "refCode": "string",
      "taxAmount": 1,
      "total": 1,
      "totalEarned": 1,
      "totalPaid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number | Affiliate ID for the pending payout. |
| `amount` | number | Amount available to pay. |
| `amountAfterTax` | number | Amount after tax. |
| `amounts.mlmReward` | number | MLM reward amount. |
| `amounts.paid` | number | Paid amount. |
| `amounts.salesCommission` | number | Sales commission amount. |
| `email` | string | Affiliate email address. |
| `name` | string | Affiliate name. |
| `paidOut` | number | Amount already paid out. |
| `pending` | number | Pending amount. |
| `refCode` | string | Affiliate referral code. |
| `taxAmount` | number | Tax amount. |
| `total` | number | Total pending payout amount. |
| `totalEarned` | number | Total earned amount. |
| `totalPaid` | number | Total paid amount. |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/payments/pending` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pending-payouts.md) for the provider-specific parameters and requirements.

