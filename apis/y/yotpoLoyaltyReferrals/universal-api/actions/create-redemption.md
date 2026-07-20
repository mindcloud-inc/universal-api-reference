# Yotpo Loyalty & Referrals: Create Redemption

Creates a redemption in Yotpo Loyalty & Referrals.

```
POST https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-redemption" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "redemptionOptionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/create-redemption', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "redemptionOptionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `redemptionOptionId` | number | yes | Unique identifier of the redemption option being redeemed. |
| `customerEmail` | string | no | Customer email address. Use one customer identifier for the redemption request. |
| `posAccountId` | string | no | Customer identifier from your POS system. Use one customer identifier for the redemption request. |
| `phoneNumber` | string | no | Customer phone number in E.164 format. Use one customer identifier for the redemption request. |
| `customerId` | string | no | Customer identifier from your system. Use one customer identifier for the redemption request. |
| `delayPointsDeduction` | boolean | no | Only deduct points when the associated order is later received. |
| `currency` | string | no | Currency code to use when the account is configured for multi-currency. |
| `pointsToRedeem` | number | no | Point amount to redeem for variable redemptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "approvedAt": "string",
      "atCheckout": true,
      "code": "string",
      "createdAt": "string",
      "id": 1,
      "isAdmin": true,
      "isPos": true,
      "rewardText": "string",
      "thirdPartyId": "string",
      "thirdPartyRuleId": "string",
      "token": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean | Whether the redemption has been approved. |
| `approvedAt` | string | Timestamp when the redemption was approved, when available. |
| `atCheckout` | boolean | Whether the redemption is associated with checkout. |
| `code` | string | Generated redemption code, when available. |
| `createdAt` | string | Timestamp when the redemption was created. |
| `id` | number | Unique identifier for the redemption record. |
| `isAdmin` | boolean | Whether the redemption was created by an admin flow. |
| `isPos` | boolean | Whether the redemption was created from a POS flow. |
| `rewardText` | string | Reward text or generated redemption text returned by Yotpo. |
| `thirdPartyId` | string | Third-party identifier for the generated code, when available. |
| `thirdPartyRuleId` | string | Third-party rule identifier for the generated code, when available. |
| `token` | string | Redemption token returned by Yotpo. |
| `updatedAt` | string | Timestamp when the redemption was last updated. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `POST /api/v2/redemptions` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-redemption.md) for the provider-specific parameters and requirements.

