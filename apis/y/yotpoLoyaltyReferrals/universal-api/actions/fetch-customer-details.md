# Yotpo Loyalty & Referrals: Fetch Customer Details

Retrieves customer details from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-customer-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-customer-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-customer-details?${params}`, {
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
| `customerEmail` | string | no | The customer's email address. Required if no pos_account_id, customer_id, or phone_number is passed. |
| `customerId` | string | no | The identifier used to uniquely identify the customer in your system. Required if no customer_email, pos_account_id, or phone_number is passed. |
| `posAccountId` | string | no | The identifier used to uniquely identify the customer in your POS system. Required if no customer_email, customer_id, or phone_number is passed. |
| `phoneNumber` | string | no | The customer's phone number in E.164 format. Required if no customer_email, pos_account_id, or customer_id is passed. |
| `countryIsoCode` | string | no | Only use if phone_number cannot be sent in full E.164 format. |
| `withReferralCode` | boolean | no | Return referral code information when set to true. Default: `false`. |
| `withHistory` | boolean | no | Return point earning and redemption history when set to true. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditBalance": "string",
      "creditBalanceInCustomerCurrency": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasStoreAccount": true,
      "historyItems": [
        {}
      ],
      "lastName": "Chen",
      "lastPurchaseAt": "string",
      "lastSeenAt": "string",
      "nextPointsExpireAmount": 1,
      "nextPointsExpireOn": "string",
      "optedInAt": "string",
      "optIn": true,
      "perksRedeemed": 1,
      "phoneNumber": "string",
      "pointsBalance": 1,
      "pointsEarned": 1,
      "pointsExpireAt": "string",
      "posAccountId": "string",
      "thirdPartyId": "string",
      "thirtyPartyId": "string",
      "totalPurchases": 1,
      "totalSpendCents": 1,
      "vipTierActionsCompleted": {},
      "vipTierEntryDate": "string",
      "vipTierExpiration": "string",
      "vipTierMaintenanceRequirements": {},
      "vipTierName": "Ava Chen",
      "vipTierUpgradeRequirements": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditBalance` | string | Customer credit balance in store currency. |
| `creditBalanceInCustomerCurrency` | string | Customer credit balance in the customer's currency. |
| `email` | string | Customer email address. |
| `firstName` | string | Customer first name. |
| `hasStoreAccount` | boolean | Whether the customer has a store account. |
| `historyItems` | array<object> | Point earning and redemption history items returned when history is requested. |
| `lastName` | string | Customer last name. |
| `lastPurchaseAt` | string | Timestamp of the customer's most recent purchase. |
| `lastSeenAt` | string | Timestamp when the customer was last seen. |
| `nextPointsExpireAmount` | number | Amount of points expiring next. |
| `nextPointsExpireOn` | string | Date of the next points expiration event. |
| `optedInAt` | string | Date when the customer opted in. |
| `optIn` | boolean | Whether the customer has opted in. |
| `perksRedeemed` | number | Number of perks the customer has redeemed. |
| `phoneNumber` | string | Customer phone number when available. |
| `pointsBalance` | number | Current points balance. |
| `pointsEarned` | number | Total points earned by the customer. |
| `pointsExpireAt` | string | Timestamp when the customer's points expire. |
| `posAccountId` | string | POS account identifier when available. |
| `thirdPartyId` | string | Third-party customer identifier when available. |
| `thirtyPartyId` | string | Provider legacy typo field mapped from `thirty_party_id`. |
| `totalPurchases` | number | Total number of purchases recorded for the customer. |
| `totalSpendCents` | number | Customer lifetime spend in cents. |
| `vipTierActionsCompleted` | object | Progress already completed toward the current VIP tier thresholds. |
| `vipTierEntryDate` | string | Timestamp when the customer entered the current VIP tier. |
| `vipTierExpiration` | string | Timestamp when the current VIP tier expires. |
| `vipTierMaintenanceRequirements` | object | Requirements needed to maintain the current VIP tier. |
| `vipTierName` | string | Current VIP tier name when the merchant uses VIP tiers. |
| `vipTierUpgradeRequirements` | object | Requirements needed to upgrade to the next VIP tier. |

## Native endpoint

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/customers` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-customer-details.md) for the provider-specific parameters and requirements.

