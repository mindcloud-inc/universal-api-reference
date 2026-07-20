# Finmo: Create Payout

Creates a new payout in Finmo.

```
POST https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderAmount": 1,
  "senderCurrency": "string",
  "beneficiaryAmount": 1,
  "beneficiaryCurrency": "string",
  "payoutMethodName": "Ava Chen",
  "purposeCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderAmount": 1,
    "senderCurrency": "string",
    "beneficiaryAmount": 1,
    "beneficiaryCurrency": "string",
    "payoutMethodName": "Ava Chen",
    "purposeCode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderAmount` | number | yes |  |
| `senderCurrency` | string | yes |  |
| `senderCountry` | string | no |  |
| `beneficiaryAmount` | number | yes |  |
| `beneficiaryCurrency` | string | yes |  |
| `beneficiaryCountry` | string | no |  |
| `payoutMethodName` | string | yes |  |
| `fxRateId` | string | no |  |
| `debitWalletId` | string | no |  |
| `feesWalletId` | string | no |  |
| `organizationReferenceId` | string | no |  |
| `description` | string | no |  |
| `payoutMethodParam` | object | no |  |
| `payoutBeneficiaryParam` | object | no |  |
| `payoutControls` | object | no |  |
| `payoutBeneficiaryId` | string | no |  |
| `payoutSenderId` | string | no |  |
| `payoutSenderParam` | object | no |  |
| `purposeCode` | string | yes |  |
| `receiptEmail` | string | no |  |
| `payoutReference` | string | no |  |
| `webhookUrl` | string | no |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accountPayableId": {},
        "additionalData": {},
        "beneficiaryAmount": 1,
        "beneficiaryCountry": "string",
        "beneficiaryCurrency": "string",
        "bulkPayoutId": {},
        "createdAt": "string",
        "customerId": {},
        "debitWalletId": "string",
        "debitWalletTransactionId": "string",
        "description": "string",
        "estimatedDeliveryAt": {},
        "feesCurrency": "string",
        "feesIncludingTax": 1,
        "feesWalletId": "string",
        "feesWalletTransactionId": "string",
        "feesWithoutTax": 1,
        "fxConversionId": {},
        "fxRate": 1,
        "fxRateId": {},
        "isChargeable": true,
        "isFeesCharged": true,
        "isPaid": true,
        "isReconciled": true,
        "isReturnable": true,
        "isReturned": true,
        "metadata": {
          "source": "string",
          "testRun": "string"
        },
        "organizationReferenceId": "string",
        "orgId": "string",
        "paidAmount": {},
        "paidAt": {},
        "paidCurrency": {},
        "payoutBeneficiaryId": {},
        "payoutBeneficiaryParam": {
          "bankCountry": "string",
          "currency": "string",
          "individual": {
            "firstName": "Ava",
            "lastName": "Chen"
          },
          "payId": "string",
          "payIdType": "string",
          "type": "string"
        },
        "payoutChargeBearer": {},
        "payoutId": "string",
        "payoutMethodName": "Ava Chen",
        "payoutMethodParam": {},
        "payoutReference": {},
        "payoutReturnedTransactionId": {},
        "payoutReturnedWalletId": {},
        "payoutReturnedWalletTransactionId": {},
        "payoutSenderId": {},
        "payoutSenderParam": {},
        "payoutType": "string",
        "pricingEventData": {
          "pAYOUTCOMPLETED": {
            "feesCurrency": "string",
            "feesIncludingTax": 1,
            "feesWithoutTax": 1,
            "taxOnFees": 1
          },
          "total": {
            "aggregatedFeesCurrency": "string",
            "aggregatedFeesIncludingTax": 1,
            "aggregatedFeesWithoutTax": 1,
            "aggregatedTaxOnFees": 1
          }
        },
        "purposeCode": "string",
        "reasonForFailure": {},
        "reasonForReturn": {},
        "receiptEmail": {},
        "releasedAt": {},
        "returnedAmount": {},
        "returnedAt": {},
        "returnedCurrency": {},
        "scope": "string",
        "senderAmount": 1,
        "senderCountry": "string",
        "senderCurrency": "string",
        "status": "string",
        "taxOnFees": {},
        "transactionId": {},
        "updatedAt": "string",
        "webhookUrl": {}
      },
      "requestId": "string",
      "requestTime": "string",
      "statusCode": 1,
      "statusText": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.accountPayableId` | object |  |
| `data.additionalData` | object |  |
| `data.beneficiaryAmount` | number |  |
| `data.beneficiaryCountry` | string |  |
| `data.beneficiaryCurrency` | string |  |
| `data.bulkPayoutId` | object |  |
| `data.createdAt` | string |  |
| `data.customerId` | object |  |
| `data.debitWalletId` | string |  |
| `data.debitWalletTransactionId` | string |  |
| `data.description` | string |  |
| `data.estimatedDeliveryAt` | object |  |
| `data.feesCurrency` | string |  |
| `data.feesIncludingTax` | number |  |
| `data.feesWalletId` | string |  |
| `data.feesWalletTransactionId` | string |  |
| `data.feesWithoutTax` | number |  |
| `data.fxConversionId` | object |  |
| `data.fxRate` | number |  |
| `data.fxRateId` | object |  |
| `data.isChargeable` | boolean |  |
| `data.isFeesCharged` | boolean |  |
| `data.isPaid` | boolean |  |
| `data.isReconciled` | boolean |  |
| `data.isReturnable` | boolean |  |
| `data.isReturned` | boolean |  |
| `data.metadata` | object |  |
| `data.metadata.source` | string |  |
| `data.metadata.testRun` | string |  |
| `data.organizationReferenceId` | string |  |
| `data.orgId` | string |  |
| `data.paidAmount` | object |  |
| `data.paidAt` | object |  |
| `data.paidCurrency` | object |  |
| `data.payoutBeneficiaryId` | object |  |
| `data.payoutBeneficiaryParam` | object |  |
| `data.payoutBeneficiaryParam.bankCountry` | string |  |
| `data.payoutBeneficiaryParam.currency` | string |  |
| `data.payoutBeneficiaryParam.individual` | object |  |
| `data.payoutBeneficiaryParam.individual.firstName` | string |  |
| `data.payoutBeneficiaryParam.individual.lastName` | string |  |
| `data.payoutBeneficiaryParam.payId` | string |  |
| `data.payoutBeneficiaryParam.payIdType` | string |  |
| `data.payoutBeneficiaryParam.type` | string |  |
| `data.payoutChargeBearer` | object |  |
| `data.payoutId` | string |  |
| `data.payoutMethodName` | string |  |
| `data.payoutMethodParam` | object |  |
| `data.payoutReference` | object |  |
| `data.payoutReturnedTransactionId` | object |  |
| `data.payoutReturnedWalletId` | object |  |
| `data.payoutReturnedWalletTransactionId` | object |  |
| `data.payoutSenderId` | object |  |
| `data.payoutSenderParam` | object |  |
| `data.payoutType` | string |  |
| `data.pricingEventData` | object |  |
| `data.pricingEventData.pAYOUTCOMPLETED` | object |  |
| `data.pricingEventData.pAYOUTCOMPLETED.feesCurrency` | string |  |
| `data.pricingEventData.pAYOUTCOMPLETED.feesIncludingTax` | number |  |
| `data.pricingEventData.pAYOUTCOMPLETED.feesWithoutTax` | number |  |
| `data.pricingEventData.pAYOUTCOMPLETED.taxOnFees` | number |  |
| `data.pricingEventData.total` | object |  |
| `data.pricingEventData.total.aggregatedFeesCurrency` | string |  |
| `data.pricingEventData.total.aggregatedFeesIncludingTax` | number |  |
| `data.pricingEventData.total.aggregatedFeesWithoutTax` | number |  |
| `data.pricingEventData.total.aggregatedTaxOnFees` | number |  |
| `data.purposeCode` | string |  |
| `data.reasonForFailure` | object |  |
| `data.reasonForReturn` | object |  |
| `data.receiptEmail` | object |  |
| `data.releasedAt` | object |  |
| `data.returnedAmount` | object |  |
| `data.returnedAt` | object |  |
| `data.returnedCurrency` | object |  |
| `data.scope` | string |  |
| `data.senderAmount` | number |  |
| `data.senderCountry` | string |  |
| `data.senderCurrency` | string |  |
| `data.status` | string |  |
| `data.taxOnFees` | object |  |
| `data.transactionId` | object |  |
| `data.updatedAt` | string |  |
| `data.webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `POST /payout` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payout.md) for the provider-specific parameters and requirements.

