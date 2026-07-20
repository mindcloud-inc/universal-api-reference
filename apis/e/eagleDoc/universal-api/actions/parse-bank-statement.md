# Eagle Doc: Parse Bank Statement

Creates a bank statement extraction in Eagle Doc.

```
POST https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-bank-statement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eagle Doc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-bank-statement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eagleDoc/latest/actions/parse-bank-statement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Bank statement file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "docType": "string",
      "general": {
        "accountHolderName": "Ava Chen",
        "accountNumber": "string",
        "accountStatus": "string",
        "accountType": "string",
        "bankName": "Ava Chen",
        "branchAddress": "string",
        "branchCode": "string",
        "branchStreet": "string",
        "closingBalance": 1,
        "currency": "string",
        "feesCharged": 1,
        "iFSCCode": "string",
        "interestEarned": "string",
        "mICRCode": "string",
        "minimumBalanceRequired": "string",
        "openingBalance": 1,
        "statementPeriod": "string",
        "sWIFTCode": "string",
        "totalDeposits": 1,
        "totalWithdrawals": 1
      },
      "lists": {
        "transactionList": [
          {
            "counterPartyName": "Ava Chen",
            "transactionAmount": 1,
            "transactionDate": "2026-05-07T12:00:00.000Z",
            "transactionDescription": {},
            "transactionType": "string"
          }
        ]
      },
      "processingInfo": {
        "docConfigId": {},
        "docType": "string",
        "duration": "string",
        "fileHash": "string",
        "language": "string",
        "numberOfPages": "string",
        "version": "string"
      },
      "signatures": {},
      "verification": {
        "nonDuplication": {
          "flagValid": true,
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `docType` | string |  |
| `general.accountHolderName` | string |  |
| `general.accountNumber` | string |  |
| `general.accountStatus` | string |  |
| `general.accountType` | string |  |
| `general.bankName` | string |  |
| `general.branchAddress` | string |  |
| `general.branchCode` | string |  |
| `general.branchStreet` | string |  |
| `general.closingBalance` | number |  |
| `general.currency` | string |  |
| `general.feesCharged` | number |  |
| `general.iFSCCode` | string |  |
| `general.interestEarned` | string |  |
| `general.mICRCode` | string |  |
| `general.minimumBalanceRequired` | string |  |
| `general.openingBalance` | number |  |
| `general.statementPeriod` | string |  |
| `general.sWIFTCode` | string |  |
| `general.totalDeposits` | number |  |
| `general.totalWithdrawals` | number |  |
| `lists.transactionList[].counterPartyName` | string |  |
| `lists.transactionList[].transactionAmount` | number |  |
| `lists.transactionList[].transactionDate` | date |  |
| `lists.transactionList[].transactionDescription` | object |  |
| `lists.transactionList[].transactionType` | string |  |
| `processingInfo.docConfigId` | object |  |
| `processingInfo.docType` | string |  |
| `processingInfo.duration` | string |  |
| `processingInfo.fileHash` | string |  |
| `processingInfo.language` | string |  |
| `processingInfo.numberOfPages` | string |  |
| `processingInfo.version` | string |  |
| `signatures` | object |  |
| `verification.nonDuplication.flagValid` | boolean |  |
| `verification.nonDuplication.message` | string |  |

## Native endpoint

Through the native Eagle Doc API, this operation is `POST /api/anydoc/v1/processing` (base URL `https://de.eagle-doc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-bank-statement.md) for the provider-specific parameters and requirements.

