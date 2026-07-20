# Vouchery.io: Get Voucher



```
GET https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-voucher
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vouchery.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-voucher?connectionId=$CONNECTION_ID&code=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "code": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voucheryio/latest/actions/get-voucher?${params}`, {
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
| `code` | string | yes | Voucher code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allocatedToCustomerAt": "string",
      "campaign": {
        "budgetCode": {},
        "channel": {},
        "createdAt": "string",
        "currency": "string",
        "currencySymbol": "string",
        "customerInformation": {},
        "description": {},
        "endAt": {},
        "giftCardValue": {},
        "id": 1,
        "isAutomated": true,
        "maxDiscount": {},
        "maxRedemptions": {},
        "maxRedemptionsUnit": 1,
        "maxTotalBudget": {},
        "maxTotalBudgetUnit": 1,
        "medium": {},
        "minimumValue": 1,
        "name": "Ava Chen",
        "parentId": 1,
        "purpose": {},
        "redemptionsCount": 1,
        "rewards": {},
        "rules": {},
        "startAt": {},
        "status": "string",
        "team": {},
        "template": "string",
        "type": "string",
        "updatedAt": "string",
        "voucherCodeType": "string",
        "voucherLifetime": {},
        "voucherMaxRedemptions": 1,
        "voucherMaxRedemptionsAmount": {},
        "voucherPrefix": "string",
        "voucherRandomPartLength": 1,
        "voucherType": "string"
      },
      "campaignId": 1,
      "code": "string",
      "createdAt": "string",
      "customer": {
        "anonymisedEmail": "ava@example.com",
        "createdAt": "string",
        "id": 1,
        "identifier": "string",
        "loyaltyPoints": 1,
        "name": "Ava Chen",
        "type": "string",
        "updatedAt": "string"
      },
      "customerId": 1,
      "expiresAt": {},
      "id": 1,
      "lastActivationAt": "string",
      "qrCodeUrl": "https://example.com",
      "redemptionsConfirmedCount": 1,
      "redemptionsLeft": 1,
      "redemptionsUnconfirmedCount": 1,
      "status": "string",
      "type": "string",
      "updatedAt": "string",
      "value": 1,
      "valueLeft": 1,
      "valueReserved": 1,
      "voucherType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `allocatedToCustomerAt` | string |  |
| `campaign.budgetCode` | object |  |
| `campaign.channel` | object |  |
| `campaign.createdAt` | string |  |
| `campaign.currency` | string |  |
| `campaign.currencySymbol` | string |  |
| `campaign.customerInformation` | object |  |
| `campaign.description` | object |  |
| `campaign.endAt` | object |  |
| `campaign.giftCardValue` | object |  |
| `campaign.id` | number |  |
| `campaign.isAutomated` | boolean |  |
| `campaign.maxDiscount` | object |  |
| `campaign.maxRedemptions` | object |  |
| `campaign.maxRedemptionsUnit` | number |  |
| `campaign.maxTotalBudget` | object |  |
| `campaign.maxTotalBudgetUnit` | number |  |
| `campaign.medium` | object |  |
| `campaign.minimumValue` | number |  |
| `campaign.name` | string |  |
| `campaign.parentId` | number |  |
| `campaign.purpose` | object |  |
| `campaign.redemptionsCount` | number |  |
| `campaign.rewards` | object |  |
| `campaign.rules` | object |  |
| `campaign.startAt` | object |  |
| `campaign.status` | string |  |
| `campaign.team` | object |  |
| `campaign.template` | string |  |
| `campaign.type` | string |  |
| `campaign.updatedAt` | string |  |
| `campaign.voucherCodeType` | string |  |
| `campaign.voucherLifetime` | object |  |
| `campaign.voucherMaxRedemptions` | number |  |
| `campaign.voucherMaxRedemptionsAmount` | object |  |
| `campaign.voucherPrefix` | string |  |
| `campaign.voucherRandomPartLength` | number |  |
| `campaign.voucherType` | string |  |
| `campaignId` | number |  |
| `code` | string |  |
| `createdAt` | string |  |
| `customer.anonymisedEmail` | string |  |
| `customer.createdAt` | string |  |
| `customer.id` | number |  |
| `customer.identifier` | string |  |
| `customer.loyaltyPoints` | number |  |
| `customer.name` | string |  |
| `customer.type` | string |  |
| `customer.updatedAt` | string |  |
| `customerId` | number |  |
| `expiresAt` | object |  |
| `id` | number |  |
| `lastActivationAt` | string |  |
| `qrCodeUrl` | string |  |
| `redemptionsConfirmedCount` | number |  |
| `redemptionsLeft` | number |  |
| `redemptionsUnconfirmedCount` | number |  |
| `status` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `value` | number |  |
| `valueLeft` | number |  |
| `valueReserved` | number |  |
| `voucherType` | string |  |

## Native endpoint

Through the native Vouchery.io API, this operation is `GET /vouchers/:code` (base URL `https://mindcloud.sandbox.vouchery.app/api/v2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-voucher.md) for the provider-specific parameters and requirements.

