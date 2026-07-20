# Yotpo Loyalty & Referrals Universal API Examples

These examples use the MindCloud API key and Yotpo Loyalty & Referrals connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Recently Updated Customers

Retrieves recently updated customers from Yotpo Loyalty & Referrals.

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

Example response:

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

See the full [Fetch Recently Updated Customers action reference](actions/fetch-recently-updated-customers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yotpoLoyaltyReferrals/latest/actions/fetch-recently-updated-customers).

## Adjust Customer Points Balance

Updates a customer's points balance in Yotpo Loyalty & Referrals.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/adjust-customer-points-balance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pointAdjustmentAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yotpoLoyaltyReferrals/latest/actions/adjust-customer-points-balance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pointAdjustmentAmount": 1
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "customerId": 1,
      "id": 1,
      "merchantId": 1,
      "name": "Ava Chen",
      "referralId": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Adjust Customer Points Balance action reference](actions/adjust-customer-points-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/yotpoLoyaltyReferrals/latest/actions/adjust-customer-points-balance).
