# Yotpo Loyalty & Referrals: Identify Referrer

Finds or creates a referral link in Yotpo Loyalty & Referrals.

```
POST https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/identify-referrer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/identify-referrer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/identify-referrer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the referring customer. |
| `firstName` | string | no | Optional first name for the referring customer. |
| `lastName` | string | no | Optional last name for the referring customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "merchantId": 1,
      "referralDiscountCode": "string",
      "referralDiscountCodeId": 1,
      "referralLink": "https://example.com",
      "referralReceipts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address of the referrer. |
| `id` | number | Unique identifier of the referring customer. |
| `merchantId` | number | Yotpo merchant identifier. |
| `referralDiscountCode` | string | Referral discount code when one is present. |
| `referralDiscountCodeId` | number | Identifier of the referral discount code when one is present. |
| `referralLink` | string | Referral link returned for the customer. |
| `referralReceipts` | array<object> | Referral receipt records associated with the referrer. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/referral/referrer` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/identify-referrer.md) for the provider-specific parameters and requirements.

