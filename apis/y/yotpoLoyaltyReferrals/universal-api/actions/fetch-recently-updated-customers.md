# Yotpo Loyalty & Referrals: Fetch Recently Updated Customers

Retrieves recently updated customers from Yotpo Loyalty & Referrals.

```
GET https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-recently-updated-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yotpo Loyalty & Referrals `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-recently-updated-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/fetch-recently-updated-customers?${params}`, {
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
      "birthDay": 1,
      "birthdayMonth": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasStoreAccount": true,
      "lastName": "Chen",
      "lastPurchaseAt": "string",
      "lastSeenAt": "string",
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
| `birthDay` | number | Customer birth day when available. |
| `birthdayMonth` | number | Customer birth month when available. |
| `email` | string | Customer email address. |
| `firstName` | string | Customer first name. |
| `hasStoreAccount` | boolean | Whether the customer has a store account. |
| `lastName` | string | Customer last name. |
| `lastPurchaseAt` | string | Timestamp of the customer's most recent purchase. |
| `lastSeenAt` | string | Timestamp when the customer was last seen. |
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

Through the native Yotpo Loyalty & Referrals API, this operation is `GET /api/v2/customers/recent` (base URL `https://loyalty.yotpo.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/fetch-recently-updated-customers.md) for the provider-specific parameters and requirements.

