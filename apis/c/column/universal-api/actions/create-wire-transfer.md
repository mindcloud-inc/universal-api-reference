# Column: Create Wire Transfer



```
POST https://connect.mindcloud.co/v1/universal/column/latest/actions/create-wire-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Column `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/column/latest/actions/create-wire-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currencyCode": "USD",
  "counterpartyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/column/latest/actions/create-wire-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currencyCode": "USD",
    "counterpartyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount in cents of the wire transfer. |
| `currencyCode` | string | yes | ISO 4217 currency code for the transfer. Default: `USD`. |
| `bankAccountId` | string | no | Bank account ID to send the wire from. Provide either Bank Account ID or Account Number ID. |
| `counterpartyId` | string | yes | Counterparty ID that will receive the wire. The counterparty must have wire details attached. |
| `description` | string | no | Description transmitted to the beneficiary bank statement. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountNumberId` | string | no | Specific account number ID to send the wire from. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountNumberId": "string",
      "allowOverdraft": true,
      "amount": 1,
      "bankAccountId": "string",
      "beneficiaryAccountNumber": "string",
      "beneficiaryName": "Ava Chen",
      "beneficiaryReference": "string",
      "businessFunctionCode": "string",
      "completedAt": {},
      "counterpartyId": "string",
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "creditorAgentName": "Ava Chen",
      "creditorAgentRoutingNumber": "string",
      "creditorTaxId": "string",
      "currencyCode": "string",
      "debtorAgentName": "Ava Chen",
      "debtorAgentRoutingNumber": "string",
      "description": "string",
      "fiToFiInformationLine1": "string",
      "fiToFiInformationLine2": "string",
      "fiToFiInformationLine3": "string",
      "fiToFiInformationLine4": "string",
      "fiToFiInformationLine5": "string",
      "fiToFiInformationLine6": "string",
      "id": "string",
      "idempotencyKey": "string",
      "imad": "string",
      "initiatedAt": "string",
      "instructedAgentName": "Ava Chen",
      "instructedAgentRoutingNumber": "string",
      "instructingAgentName": "Ava Chen",
      "instructingAgentRoutingNumber": "string",
      "isIncoming": true,
      "isOnUs": true,
      "manualReviewAt": {},
      "omad": "string",
      "originatorAccountNumber": "string",
      "originatorName": "Ava Chen",
      "originatorToBeneficiaryInformationLine1": "string",
      "originatorToBeneficiaryInformationLine2": "string",
      "originatorToBeneficiaryInformationLine3": "string",
      "originatorToBeneficiaryInformationLine4": "string",
      "pendingSubmissionAt": {},
      "previousMessageReference": "string",
      "rawBeneficiaryAddress": "string",
      "rawOriginatorAddress": "string",
      "receiverDiName": "Ava Chen",
      "receiverDiRoutingNumber": "string",
      "rejectedAt": {},
      "reversalPairTransferId": "string",
      "senderAddress": {
        "city": "string",
        "countryCode": "string",
        "line1": "string",
        "line2": "string",
        "postalCode": "string",
        "state": "string"
      },
      "senderDiName": "Ava Chen",
      "senderDiRoutingNumber": "string",
      "senderReference": "string",
      "status": "string",
      "submittedAt": {},
      "subtypeCode": "string",
      "taxRecordPeriodType": "string",
      "taxTypeCode": "string",
      "taxYear": "string",
      "typeCode": "string",
      "ultimateOriginatorCounterpartyId": "string",
      "updatedAt": "string",
      "wireDrawdownRequestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountNumberId` | string |  |
| `allowOverdraft` | boolean |  |
| `amount` | number |  |
| `bankAccountId` | string |  |
| `beneficiaryAccountNumber` | string |  |
| `beneficiaryName` | string |  |
| `beneficiaryReference` | string |  |
| `businessFunctionCode` | string |  |
| `completedAt` | object |  |
| `counterpartyId` | string |  |
| `createdAt` | string |  |
| `createdBy.id` | string |  |
| `createdBy.name` | string |  |
| `createdBy.type` | string |  |
| `creditorAgentName` | string |  |
| `creditorAgentRoutingNumber` | string |  |
| `creditorTaxId` | string |  |
| `currencyCode` | string |  |
| `debtorAgentName` | string |  |
| `debtorAgentRoutingNumber` | string |  |
| `description` | string |  |
| `fiToFiInformationLine1` | string |  |
| `fiToFiInformationLine2` | string |  |
| `fiToFiInformationLine3` | string |  |
| `fiToFiInformationLine4` | string |  |
| `fiToFiInformationLine5` | string |  |
| `fiToFiInformationLine6` | string |  |
| `id` | string |  |
| `idempotencyKey` | string |  |
| `imad` | string |  |
| `initiatedAt` | string |  |
| `instructedAgentName` | string |  |
| `instructedAgentRoutingNumber` | string |  |
| `instructingAgentName` | string |  |
| `instructingAgentRoutingNumber` | string |  |
| `isIncoming` | boolean |  |
| `isOnUs` | boolean |  |
| `manualReviewAt` | object |  |
| `omad` | string |  |
| `originatorAccountNumber` | string |  |
| `originatorName` | string |  |
| `originatorToBeneficiaryInformationLine1` | string |  |
| `originatorToBeneficiaryInformationLine2` | string |  |
| `originatorToBeneficiaryInformationLine3` | string |  |
| `originatorToBeneficiaryInformationLine4` | string |  |
| `pendingSubmissionAt` | object |  |
| `previousMessageReference` | string |  |
| `rawBeneficiaryAddress` | string |  |
| `rawOriginatorAddress` | string |  |
| `receiverDiName` | string |  |
| `receiverDiRoutingNumber` | string |  |
| `rejectedAt` | object |  |
| `reversalPairTransferId` | string |  |
| `senderAddress.city` | string |  |
| `senderAddress.countryCode` | string |  |
| `senderAddress.line1` | string |  |
| `senderAddress.line2` | string |  |
| `senderAddress.postalCode` | string |  |
| `senderAddress.state` | string |  |
| `senderDiName` | string |  |
| `senderDiRoutingNumber` | string |  |
| `senderReference` | string |  |
| `status` | string |  |
| `submittedAt` | object |  |
| `subtypeCode` | string |  |
| `taxRecordPeriodType` | string |  |
| `taxTypeCode` | string |  |
| `taxYear` | string |  |
| `typeCode` | string |  |
| `ultimateOriginatorCounterpartyId` | string |  |
| `updatedAt` | string |  |
| `wireDrawdownRequestId` | string |  |

## Native endpoint

Through the native Column API, this operation is `POST /transfers/wire` (base URL `https://api.column.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wire-transfer.md) for the provider-specific parameters and requirements.

