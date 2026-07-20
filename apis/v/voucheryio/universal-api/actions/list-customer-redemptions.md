# Vouchery.io: List Customer Redemptions



```
GET https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/list-customer-redemptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/list-customer-redemptions?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/list-customer-redemptions?${params}`, {
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
| `identifier` | string | yes | Customer Identifier |
| `page` | number | no | Result page (indexed from 1) |
| `perPage` | number | no | Results per page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "currency": "string",
        "currencySymbol": "string",
        "id": 1,
        "name": "Ava Chen",
        "parentId": 1,
        "template": "string",
        "type": "string",
        "voucherMaxRedemptions": 1,
        "voucherType": "string"
      },
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
      "id": 1,
      "totalTransactionCost": 1,
      "transactionId": "string",
      "type": "string",
      "updatedAt": "string",
      "userAgent": {},
      "validatedAt": "string",
      "valueLeft": {},
      "voucher": {
        "code": "string",
        "createdAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.currency` | string |  |
| `campaign.currencySymbol` | string |  |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.parentId` | number |  |
| `campaign.template` | string |  |
| `campaign.type` | string |  |
| `campaign.voucherMaxRedemptions` | number |  |
| `campaign.voucherType` | string |  |
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
| `id` | number |  |
| `totalTransactionCost` | number |  |
| `transactionId` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `userAgent` | object |  |
| `validatedAt` | string |  |
| `valueLeft` | object |  |
| `voucher.code` | string |  |
| `voucher.createdAt` | string |  |

## Native endpoint

Through the native Vouchery.io API, this operation is `GET /customers/:identifier/redemptions` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-redemptions.md) for the provider-specific parameters and requirements.

