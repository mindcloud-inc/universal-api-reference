# Airwallex: Create Transfer

Creates a new payout transfer in Airwallex.

```
POST https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/create-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/create-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "beneficiaryId": "string",
  "transferAmount": "string",
  "transferCurrency": "string",
  "transferMethod": "string",
  "reason": "string",
  "reference": "string",
  "requestId": "string",
  "sourceCurrency": "string",
  "lockRateOnCreate": true,
  "transferDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/create-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "beneficiaryId": "string",
    "transferAmount": "string",
    "transferCurrency": "string",
    "transferMethod": "string",
    "reason": "string",
    "reference": "string",
    "requestId": "string",
    "sourceCurrency": "string",
    "lockRateOnCreate": true,
    "transferDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beneficiaryId` | string | yes | The saved Airwallex beneficiary ID to pay. |
| `transferAmount` | string | yes | The amount to send to the beneficiary. |
| `transferCurrency` | string | yes | The payout currency, such as USD. |
| `transferMethod` | string | yes | The payout transfer method, such as LOCAL. |
| `reason` | string | yes | The transfer purpose or payout reason. |
| `reference` | string | yes | A transfer reference visible to the payer. |
| `requestId` | string | yes | A unique idempotency key for the transfer request. |
| `sourceCurrency` | string | yes | The source wallet currency used to fund the payout. |
| `lockRateOnCreate` | boolean | yes | Whether to lock the FX rate at creation time. |
| `transferDate` | string | yes | The scheduled transfer date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountBeneficiaryReceives": 1,
      "amountPayerPays": 1,
      "beneficiary": {
        "additionalInfo": {
          "personalIdNumber": "string",
          "personalIdType": "string",
          "personalMobileNumber": "string"
        },
        "address": {
          "city": "string",
          "countryCode": "string",
          "postcode": "string",
          "state": "string",
          "streetAddress": "string"
        },
        "bankDetails": {
          "accountCurrency": "string",
          "accountName": "Ava Chen",
          "accountNumber": "string",
          "accountRoutingType1": "string",
          "accountRoutingValue1": "string",
          "bankAccountCategory": "string",
          "bankCountryCode": "string",
          "bankName": "Ava Chen",
          "localClearingSystem": "string"
        },
        "dateOfBirth": "2026-05-07T12:00:00.000Z",
        "entityType": "string",
        "type": "string"
      },
      "beneficiaryId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "feeAmount": 1,
      "feeCurrency": "string",
      "feePaidBy": "string",
      "funding": {
        "status": "string"
      },
      "id": "string",
      "payer": {
        "additionalInfo": {
          "businessIncorporationDate": "2026-05-07T12:00:00.000Z",
          "businessRegistrationNumber": "string",
          "businessRegistrationType": "string"
        },
        "address": {
          "city": "string",
          "countryCode": "string",
          "postcode": "string",
          "state": "string",
          "streetAddress": "string"
        },
        "companyName": "Ava Chen",
        "entityType": "string"
      },
      "reason": "string",
      "reference": "string",
      "remarks": "string",
      "requestId": "string",
      "shortReferenceId": "string",
      "sourceAmount": 1,
      "sourceCurrency": "string",
      "status": "string",
      "swiftChargeOption": "string",
      "transferAmount": 1,
      "transferCurrency": "string",
      "transferDate": "2026-05-07T12:00:00.000Z",
      "transferMethod": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountBeneficiaryReceives` | number |  |
| `amountPayerPays` | number |  |
| `beneficiary.additionalInfo.personalIdNumber` | string |  |
| `beneficiary.additionalInfo.personalIdType` | string |  |
| `beneficiary.additionalInfo.personalMobileNumber` | string |  |
| `beneficiary.address.city` | string |  |
| `beneficiary.address.countryCode` | string |  |
| `beneficiary.address.postcode` | string |  |
| `beneficiary.address.state` | string |  |
| `beneficiary.address.streetAddress` | string |  |
| `beneficiary.bankDetails.accountCurrency` | string |  |
| `beneficiary.bankDetails.accountName` | string |  |
| `beneficiary.bankDetails.accountNumber` | string |  |
| `beneficiary.bankDetails.accountRoutingType1` | string |  |
| `beneficiary.bankDetails.accountRoutingValue1` | string |  |
| `beneficiary.bankDetails.bankAccountCategory` | string |  |
| `beneficiary.bankDetails.bankCountryCode` | string |  |
| `beneficiary.bankDetails.bankName` | string |  |
| `beneficiary.bankDetails.localClearingSystem` | string |  |
| `beneficiary.dateOfBirth` | date |  |
| `beneficiary.entityType` | string |  |
| `beneficiary.type` | string |  |
| `beneficiaryId` | string |  |
| `createdAt` | date |  |
| `feeAmount` | number |  |
| `feeCurrency` | string |  |
| `feePaidBy` | string |  |
| `funding.status` | string |  |
| `id` | string |  |
| `payer.additionalInfo.businessIncorporationDate` | date |  |
| `payer.additionalInfo.businessRegistrationNumber` | string |  |
| `payer.additionalInfo.businessRegistrationType` | string |  |
| `payer.address.city` | string |  |
| `payer.address.countryCode` | string |  |
| `payer.address.postcode` | string |  |
| `payer.address.state` | string |  |
| `payer.address.streetAddress` | string |  |
| `payer.companyName` | string |  |
| `payer.entityType` | string |  |
| `reason` | string |  |
| `reference` | string |  |
| `remarks` | string |  |
| `requestId` | string |  |
| `shortReferenceId` | string |  |
| `sourceAmount` | number |  |
| `sourceCurrency` | string |  |
| `status` | string |  |
| `swiftChargeOption` | string |  |
| `transferAmount` | number |  |
| `transferCurrency` | string |  |
| `transferDate` | date |  |
| `transferMethod` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Airwallex API, this operation is `POST /api/v1/transfers/create` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transfer.md) for the provider-specific parameters and requirements.

