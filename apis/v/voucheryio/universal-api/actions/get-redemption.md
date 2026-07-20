# Vouchery.io: Get Redemption



```
GET https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-redemption?connectionId=$CONNECTION_ID&redemptionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "redemptionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-redemption?${params}`, {
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
| `redemptionId` | number | yes | Redemption ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "budgetCode": {},
        "channel": {},
        "currency": "string",
        "currencySymbol": "string",
        "customerInformation": {},
        "description": {},
        "endAt": {},
        "id": 1,
        "medium": {},
        "name": "Ava Chen",
        "parentId": 1,
        "purpose": {},
        "startAt": {},
        "team": {},
        "template": "string",
        "type": "string",
        "voucherMaxRedemptions": 1,
        "voucherMaxRedemptionsAmount": {},
        "voucherType": "string"
      },
      "cancelledAt": {},
      "confirmed": true,
      "confirmedAt": {},
      "createdAt": "string",
      "createdBy": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "customer": {
        "anonymisedEmail": "ava@example.com",
        "averageSpent": 1,
        "createdAt": "string",
        "id": 1,
        "identifier": "string",
        "loyaltyPoints": 1,
        "name": "Ava Chen",
        "redemptionsCount": 1,
        "totalDiscountRedeemed": 1,
        "totalSpent": 1,
        "type": "string",
        "updatedAt": "string",
        "vouchersAvailableCount": 1,
        "vouchersCount": 1,
        "vouchersUsedCount": 1
      },
      "expiresAt": {},
      "grantedDiscount": 1,
      "grantedShippingDiscount": 1,
      "id": 1,
      "matchingProductsCost": 1,
      "shippingCost": {},
      "totalTransactionCost": 1,
      "transactionId": "string",
      "trigger": {},
      "type": "string",
      "updatedAt": "string",
      "userAgent": {},
      "validatedAt": "string",
      "voucher": {
        "code": "string",
        "createdAt": "string",
        "giftCardValueLeft": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.budgetCode` | object |  |
| `campaign.channel` | object |  |
| `campaign.currency` | string |  |
| `campaign.currencySymbol` | string |  |
| `campaign.customerInformation` | object |  |
| `campaign.description` | object |  |
| `campaign.endAt` | object |  |
| `campaign.id` | number |  |
| `campaign.medium` | object |  |
| `campaign.name` | string |  |
| `campaign.parentId` | number |  |
| `campaign.purpose` | object |  |
| `campaign.startAt` | object |  |
| `campaign.team` | object |  |
| `campaign.template` | string |  |
| `campaign.type` | string |  |
| `campaign.voucherMaxRedemptions` | number |  |
| `campaign.voucherMaxRedemptionsAmount` | object |  |
| `campaign.voucherType` | string |  |
| `cancelledAt` | object |  |
| `confirmed` | boolean |  |
| `confirmedAt` | object |  |
| `createdAt` | string |  |
| `createdBy.email` | string |  |
| `createdBy.name` | string |  |
| `customer.anonymisedEmail` | string |  |
| `customer.averageSpent` | number |  |
| `customer.createdAt` | string |  |
| `customer.id` | number |  |
| `customer.identifier` | string |  |
| `customer.loyaltyPoints` | number |  |
| `customer.name` | string |  |
| `customer.redemptionsCount` | number |  |
| `customer.totalDiscountRedeemed` | number |  |
| `customer.totalSpent` | number |  |
| `customer.type` | string |  |
| `customer.updatedAt` | string |  |
| `customer.vouchersAvailableCount` | number |  |
| `customer.vouchersCount` | number |  |
| `customer.vouchersUsedCount` | number |  |
| `expiresAt` | object |  |
| `grantedDiscount` | number |  |
| `grantedShippingDiscount` | number |  |
| `id` | number |  |
| `matchingProductsCost` | number |  |
| `shippingCost` | object |  |
| `totalTransactionCost` | number |  |
| `transactionId` | string |  |
| `trigger` | object |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userAgent` | object |  |
| `validatedAt` | string |  |
| `voucher.code` | string |  |
| `voucher.createdAt` | string |  |
| `voucher.giftCardValueLeft` | number |  |

## Native endpoint

Through the native Vouchery.io API, this operation is `GET /redemptions/:redemption_id` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-redemption.md) for the provider-specific parameters and requirements.

