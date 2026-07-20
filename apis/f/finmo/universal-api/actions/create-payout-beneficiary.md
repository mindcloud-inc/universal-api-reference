# Finmo: Create Payout Beneficiary

Creates a new payout beneficiary in Finmo.

```
POST https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout-beneficiary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout-beneficiary" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "beneficiaryName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-payout-beneficiary', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "beneficiaryName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes |  |
| `beneficiaryName` | string | yes |  |
| `currency` | string | no |  |
| `company` | object | no |  |
| `individual` | object | no |  |
| `description` | string | no |  |
| `bankCountry` | string | no |  |
| `bankName` | string | no |  |
| `accountNumber` | string | no |  |
| `bsb` | string | no |  |
| `bicSwift` | string | no |  |
| `intermediaryBicSwift` | string | no |  |
| `iban` | string | no |  |
| `aba` | string | no |  |
| `sortCode` | string | no |  |
| `payId` | string | no |  |
| `payIdType` | string | no |  |
| `ifsc` | string | no |  |
| `branchCode` | string | no |  |
| `bankCode` | string | no |  |
| `organizationReferenceId` | string | no |  |
| `metadata` | object | no |  |
| `proxyType` | string | no |  |
| `proxyValue` | string | no |  |
| `payoutBeneficiaryControls` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "aba": {},
        "accountNumber": "string",
        "accountType": {},
        "additionalData": {},
        "bankCity": {},
        "bankCode": {},
        "bankCountry": {},
        "bankName": {},
        "bankState": {},
        "beneficiaryName": "Ava Chen",
        "bicSwift": {},
        "billerCode": {},
        "branchCode": {},
        "bsb": "string",
        "createdAt": "string",
        "createdBy": "string",
        "currency": "string",
        "customerReferenceNumber": {},
        "description": "string",
        "duitnowProxyType": {},
        "duitnowProxyValue": {},
        "fpsProxyType": {},
        "fpsProxyValue": {},
        "iban": {},
        "ifsc": {},
        "individual": {
          "addressCity": {},
          "addressCountry": {},
          "addressLine1": {},
          "addressLine2": {},
          "addressState": {},
          "addressZipCode": {},
          "countryOfResidence": {},
          "dob": {},
          "email": {},
          "firstName": "Ava",
          "identificationCustomType": {},
          "identificationType": {},
          "identificationValue": {},
          "lastName": "Chen",
          "nationality": {},
          "phoneCountryCode": {},
          "phoneNumber": {},
          "phoneNumberE164": {},
          "registrationNumber": {}
        },
        "interacEmail": {},
        "intermediaryBicSwift": {},
        "isActive": true,
        "metadata": {
          "source": "string",
          "testRun": "string"
        },
        "nickname": {},
        "organizationReferenceId": "string",
        "orgId": "string",
        "payId": {},
        "payIdType": {},
        "payoutBeneficiaryId": "string",
        "proxyType": {},
        "proxyValue": {},
        "sortCode": {},
        "type": "string",
        "updatedAt": "string",
        "upiId": {}
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
| `data.aba` | object |  |
| `data.accountNumber` | string |  |
| `data.accountType` | object |  |
| `data.additionalData` | object |  |
| `data.bankCity` | object |  |
| `data.bankCode` | object |  |
| `data.bankCountry` | object |  |
| `data.bankName` | object |  |
| `data.bankState` | object |  |
| `data.beneficiaryName` | string |  |
| `data.bicSwift` | object |  |
| `data.billerCode` | object |  |
| `data.branchCode` | object |  |
| `data.bsb` | string |  |
| `data.createdAt` | string |  |
| `data.createdBy` | string |  |
| `data.currency` | string |  |
| `data.customerReferenceNumber` | object |  |
| `data.description` | string |  |
| `data.duitnowProxyType` | object |  |
| `data.duitnowProxyValue` | object |  |
| `data.fpsProxyType` | object |  |
| `data.fpsProxyValue` | object |  |
| `data.iban` | object |  |
| `data.ifsc` | object |  |
| `data.individual` | object |  |
| `data.individual.addressCity` | object |  |
| `data.individual.addressCountry` | object |  |
| `data.individual.addressLine1` | object |  |
| `data.individual.addressLine2` | object |  |
| `data.individual.addressState` | object |  |
| `data.individual.addressZipCode` | object |  |
| `data.individual.countryOfResidence` | object |  |
| `data.individual.dob` | object |  |
| `data.individual.email` | object |  |
| `data.individual.firstName` | string |  |
| `data.individual.identificationCustomType` | object |  |
| `data.individual.identificationType` | object |  |
| `data.individual.identificationValue` | object |  |
| `data.individual.lastName` | string |  |
| `data.individual.nationality` | object |  |
| `data.individual.phoneCountryCode` | object |  |
| `data.individual.phoneNumber` | object |  |
| `data.individual.phoneNumberE164` | object |  |
| `data.individual.registrationNumber` | object |  |
| `data.interacEmail` | object |  |
| `data.intermediaryBicSwift` | object |  |
| `data.isActive` | boolean |  |
| `data.metadata` | object |  |
| `data.metadata.source` | string |  |
| `data.metadata.testRun` | string |  |
| `data.nickname` | object |  |
| `data.organizationReferenceId` | string |  |
| `data.orgId` | string |  |
| `data.payId` | object |  |
| `data.payIdType` | object |  |
| `data.payoutBeneficiaryId` | string |  |
| `data.proxyType` | object |  |
| `data.proxyValue` | object |  |
| `data.sortCode` | object |  |
| `data.type` | string |  |
| `data.updatedAt` | string |  |
| `data.upiId` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `POST /payout-beneficiary` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payout-beneficiary.md) for the provider-specific parameters and requirements.

