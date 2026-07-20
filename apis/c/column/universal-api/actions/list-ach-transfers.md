# Column: List ACH Transfers



```
GET https://connect.mindcloud.co/v1/universal/column/latest/actions/list-ach-transfers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/column/latest/actions/list-ach-transfers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/column/latest/actions/list-ach-transfers?${params}`, {
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
| `bankAccountId` | string | no | Filter ACH transfers associated with this bank account. |
| `counterpartyId` | string | no | Filter ACH transfers associated with this counterparty. |
| `status` | string | no | Filter ACH transfers by status. |
| `isIncoming` | boolean | no | Whether to return incoming or outgoing ACH transfers. |
| `type` | string | no | ACH transfer direction filter: CREDIT or DEBIT. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "transfers": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `transfers[].accountNumberId` | string |  |
| `transfers[].acknowledgedAt` | object |  |
| `transfers[].allowOverdraft` | boolean |  |
| `transfers[].amount` | number |  |
| `transfers[].bankAccountId` | string |  |
| `transfers[].cancelledAt` | object |  |
| `transfers[].companyDiscretionaryData` | string |  |
| `transfers[].companyEntryDescription` | string |  |
| `transfers[].companyId` | string |  |
| `transfers[].companyName` | string |  |
| `transfers[].completedAt` | object |  |
| `transfers[].counterpartyId` | string |  |
| `transfers[].createdAt` | string |  |
| `transfers[].createdBy.id` | string |  |
| `transfers[].createdBy.name` | string |  |
| `transfers[].createdBy.type` | string |  |
| `transfers[].currencyCode` | string |  |
| `transfers[].description` | string |  |
| `transfers[].effectiveOn` | string |  |
| `transfers[].entryClassCode` | string |  |
| `transfers[].entryDetails.transactionCode` | number |  |
| `transfers[].entryDetails.transactionCodeName` | string |  |
| `transfers[].iat` | object |  |
| `transfers[].id` | string |  |
| `transfers[].idempotencyKey` | string |  |
| `transfers[].initiatedAt` | string |  |
| `transfers[].intermediaryFinancialInstitutions` | object |  |
| `transfers[].isIncoming` | boolean |  |
| `transfers[].isOnUs` | boolean |  |
| `transfers[].manualReviewAt` | object |  |
| `transfers[].notificationOfChanges` | object |  |
| `transfers[].nsfDeadline` | object |  |
| `transfers[].odfiRoutingNumber` | string |  |
| `transfers[].paymentRelatedInfo` | string |  |
| `transfers[].receiverId` | string |  |
| `transfers[].receiverName` | string |  |
| `transfers[].returnContestedAt` | object |  |
| `transfers[].returnDishonoredAt` | object |  |
| `transfers[].returnDishonoredFundsUnlockedAt` | object |  |
| `transfers[].returnedAt` | object |  |
| `transfers[].reversalPairTransferId` | string |  |
| `transfers[].sameDay` | boolean |  |
| `transfers[].settledAt` | object |  |
| `transfers[].status` | string |  |
| `transfers[].submittedAt` | object |  |
| `transfers[].traceNumber` | string |  |
| `transfers[].transactionTypeCode` | string |  |
| `transfers[].type` | string |  |
| `transfers[].ultimateBeneficiaryCounterpartyId` | string |  |
| `transfers[].ultimateOriginatorCounterpartyId` | string |  |
| `transfers[].updatedAt` | string |  |

## Native endpoint

Through the native Column API, this operation is `GET /transfers/ach` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-ach-transfers.md) for the provider-specific parameters and requirements.

