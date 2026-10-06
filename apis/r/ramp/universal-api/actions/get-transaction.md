# Ramp: Get Transaction



```
GET https://connect.mindcloud.co/v1/universal/ramp/latest/actions/get-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ramp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ramp/latest/actions/get-transaction?connectionId=$CONNECTION_ID&limit=25&offset=0&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ramp/latest/actions/get-transaction?${params}`, {
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
| `transactionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "merchantName": "Ava Chen",
      "amount": 1,
      "currencyCode": "string",
      "state": "string",
      "accountingDate": "string",
      "settlementDate": "string",
      "userTransactionTime": "string",
      "merchantDescriptor": "string",
      "merchantCategoryCode": "string",
      "merchantCategoryCodeDescription": "string",
      "skCategoryName": "Ava Chen",
      "skCategoryId": 1,
      "memo": "string",
      "syncStatus": "string",
      "syncedAt": "string",
      "cardPresent": true,
      "cardId": "string",
      "cardHolder": {},
      "entityId": "string",
      "entityAmount": {},
      "merchantAmount": {},
      "merchantId": "string",
      "merchantLocation": {},
      "networkMerchantId": "string",
      "originalTransactionId": "string",
      "originalTransactionAmount": {},
      "tripId": "string",
      "tripName": "Ava Chen",
      "limitId": "string",
      "fundId": "string",
      "receiptAffidavit": "string",
      "allRequirementsMetAndApproved": true,
      "minorUnitConversionRate": 1,
      "updatedAt": "string",
      "accountingCategories": [
        {}
      ],
      "accountingFieldSelections": [
        {}
      ],
      "lineItems": [
        {}
      ],
      "receipts": [
        "string"
      ],
      "disputes": [
        {}
      ],
      "policyViolations": [
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
| `id` | string |  |
| `merchantName` | string |  |
| `amount` | number |  |
| `currencyCode` | string |  |
| `state` | string |  |
| `accountingDate` | string |  |
| `settlementDate` | string |  |
| `userTransactionTime` | string |  |
| `merchantDescriptor` | string |  |
| `merchantCategoryCode` | string |  |
| `merchantCategoryCodeDescription` | string |  |
| `skCategoryName` | string |  |
| `skCategoryId` | number |  |
| `memo` | string |  |
| `syncStatus` | string |  |
| `syncedAt` | string |  |
| `cardPresent` | boolean |  |
| `cardId` | string |  |
| `cardHolder` | object |  |
| `entityId` | string |  |
| `entityAmount` | object |  |
| `merchantAmount` | object |  |
| `merchantId` | string |  |
| `merchantLocation` | object |  |
| `networkMerchantId` | string |  |
| `originalTransactionId` | string |  |
| `originalTransactionAmount` | object |  |
| `tripId` | string |  |
| `tripName` | string |  |
| `limitId` | string |  |
| `fundId` | string |  |
| `receiptAffidavit` | string |  |
| `allRequirementsMetAndApproved` | boolean |  |
| `minorUnitConversionRate` | number |  |
| `updatedAt` | string |  |
| `accountingCategories` | array<object> |  |
| `accountingFieldSelections` | array<object> |  |
| `lineItems` | array<object> |  |
| `receipts` | array<string> |  |
| `disputes` | array<object> |  |
| `policyViolations` | array<object> |  |

## Native endpoint

Through the native Ramp API, this operation is `GET transactions/:transactionId` (base URL `https://api.ramp.com/developer/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-transaction.md) for the provider-specific parameters and requirements.

