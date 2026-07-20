# Column: Get ACH Transfer



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/get-ach-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/get-ach-transfer?connectionId=$CONNECTION_ID&achTransferId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "achTransferId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/get-ach-transfer?${params}`, {
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
| `achTransferId` | string | yes | ID of the ACH transfer to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumberId": "string",
      "acknowledgedAt": {},
      "allowOverdraft": true,
      "amount": 1,
      "bankAccountId": "string",
      "cancelledAt": {},
      "companyDiscretionaryData": "string",
      "companyEntryDescription": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "completedAt": {},
      "counterpartyId": "string",
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "currencyCode": "string",
      "description": "string",
      "effectiveOn": "string",
      "entryClassCode": "string",
      "entryDetails": {
        "transactionCode": 1,
        "transactionCodeName": "Ava Chen"
      },
      "iat": {},
      "id": "string",
      "idempotencyKey": "string",
      "initiatedAt": "string",
      "intermediaryFinancialInstitutions": {},
      "isIncoming": true,
      "isOnUs": true,
      "manualReviewAt": {},
      "notificationOfChanges": {},
      "nsfDeadline": {},
      "odfiRoutingNumber": "string",
      "paymentRelatedInfo": "string",
      "receiverId": "string",
      "receiverName": "Ava Chen",
      "returnContestedAt": {},
      "returnDishonoredAt": {},
      "returnDishonoredFundsUnlockedAt": {},
      "returnedAt": {},
      "reversalPairTransferId": "string",
      "sameDay": true,
      "settledAt": "string",
      "status": "string",
      "submittedAt": "string",
      "traceNumber": "string",
      "transactionTypeCode": "string",
      "type": "string",
      "ultimateBeneficiaryCounterpartyId": "string",
      "ultimateOriginatorCounterpartyId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumberId` | string |  |
| `acknowledgedAt` | object |  |
| `allowOverdraft` | boolean |  |
| `amount` | number |  |
| `bankAccountId` | string |  |
| `cancelledAt` | object |  |
| `companyDiscretionaryData` | string |  |
| `companyEntryDescription` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `completedAt` | object |  |
| `counterpartyId` | string |  |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `currencyCode` | string |  |
| `description` | string |  |
| `effectiveOn` | string |  |
| `entryClassCode` | string |  |
| `entryDetails.transactionCode` | number |  |
| `entryDetails.transactionCodeName` | string |  |
| `iat` | object |  |
| `id` | string |  |
| `idempotencyKey` | string |  |
| `initiatedAt` | string |  |
| `intermediaryFinancialInstitutions` | object |  |
| `isIncoming` | boolean |  |
| `isOnUs` | boolean |  |
| `manualReviewAt` | object |  |
| `notificationOfChanges` | object |  |
| `nsfDeadline` | object |  |
| `odfiRoutingNumber` | string |  |
| `paymentRelatedInfo` | string |  |
| `receiverId` | string |  |
| `receiverName` | string |  |
| `returnContestedAt` | object |  |
| `returnDishonoredAt` | object |  |
| `returnDishonoredFundsUnlockedAt` | object |  |
| `returnedAt` | object |  |
| `reversalPairTransferId` | string |  |
| `sameDay` | boolean |  |
| `settledAt` | string |  |
| `status` | string |  |
| `submittedAt` | string |  |
| `traceNumber` | string |  |
| `transactionTypeCode` | string |  |
| `type` | string |  |
| `ultimateBeneficiaryCounterpartyId` | string |  |
| `ultimateOriginatorCounterpartyId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Column API, this operation is `GET /transfers/ach/:ach_transfer_id` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ach-transfer.md) for the provider-specific parameters and requirements.

