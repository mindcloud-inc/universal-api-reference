# Yotpo Loyalty & Referrals: Send Referral Emails

Sends referral emails from Yotpo Loyalty & Referrals.

```
POST https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/send-referral-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/send-referral-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/send-referral-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "emails": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address of the referring customer. |
| `customerId` | string | no | Customer identifier for the referring customer. |
| `emails` | string | yes | Comma-separated list of email addresses to share the referral link with. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yotpo Loyalty & Referrals API returns.

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/referral/share` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-referral-emails.md) for the provider-specific parameters and requirements.

