# Column: Create ACH Transfer



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-ach-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-ach-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currencyCode": "USD",
  "counterpartyId": "string",
  "type": "string",
  "entryClassCode": "PPD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-ach-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currencyCode": "USD",
    "counterpartyId": "string",
    "type": "string",
    "entryClassCode": "PPD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount in cents of the ACH transfer. |
| `currencyCode` | string | yes | ISO 4217 currency code for the transfer. Default: `USD`. |
| `bankAccountId` | string | no | Column bank account ID to send the transfer from. Provide either Bank Account ID or Account Number ID. |
| `counterpartyId` | string | yes | Counterparty ID that will receive the transfer. |
| `type` | string | yes | ACH transfer direction: CREDIT or DEBIT. |
| `entryClassCode` | string | yes | ACH Standard Entry Class code. Default: `PPD`. |
| `description` | string | no | Internal description visible in your platform. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountNumberId` | string | no | Specific Column account number ID to send the transfer from. |
| `effectiveDate` | date | no | Effective date in YYYY-MM-DD format. |
| `sameDay` | boolean | no | Whether to submit the ACH transfer as same-day ACH. |

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
      "entryDetails": {},
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
      "settledAt": {},
      "status": "string",
      "submittedAt": {},
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
| `entryDetails` | object |  |
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
| `settledAt` | object |  |
| `status` | string |  |
| `submittedAt` | object |  |
| `traceNumber` | string |  |
| `transactionTypeCode` | string |  |
| `type` | string |  |
| `ultimateBeneficiaryCounterpartyId` | string |  |
| `ultimateOriginatorCounterpartyId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Column API, this operation is `POST /transfers/ach` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ach-transfer.md) for the provider-specific parameters and requirements.

