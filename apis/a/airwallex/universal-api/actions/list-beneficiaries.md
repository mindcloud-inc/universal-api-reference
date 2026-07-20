# Airwallex: List Beneficiaries

Retrieves saved payout beneficiaries from Airwallex.

```
GET https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/list-beneficiaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/list-beneficiaries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/list-beneficiaries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "beneficiary": {
        "additionalInfo": {
          "businessRegistrationNumber": "string",
          "legalRepFirstNameInChinese": "Ava",
          "legalRepIdNumber": "string",
          "legalRepLastNameInChinese": "Chen",
          "personalFirstNameInChinese": "Ava",
          "personalIdNumber": "string",
          "personalIdType": "string",
          "personalLastNameInChinese": "Chen",
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
          "accountRoutingType2": "string",
          "accountRoutingValue1": "string",
          "accountRoutingValue2": "string",
          "bankBranch": "string",
          "bankCountryCode": "string",
          "bankName": "Ava Chen"
        },
        "dateOfBirth": "2026-05-07T12:00:00.000Z",
        "entityType": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "type": "string"
      },
      "id": "string",
      "payerEntityType": "string",
      "transferMethods": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `beneficiary.additionalInfo.businessRegistrationNumber` | string |  |
| `beneficiary.additionalInfo.legalRepFirstNameInChinese` | string |  |
| `beneficiary.additionalInfo.legalRepIdNumber` | string |  |
| `beneficiary.additionalInfo.legalRepLastNameInChinese` | string |  |
| `beneficiary.additionalInfo.personalFirstNameInChinese` | string |  |
| `beneficiary.additionalInfo.personalIdNumber` | string |  |
| `beneficiary.additionalInfo.personalIdType` | string |  |
| `beneficiary.additionalInfo.personalLastNameInChinese` | string |  |
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
| `beneficiary.bankDetails.accountRoutingType2` | string |  |
| `beneficiary.bankDetails.accountRoutingValue1` | string |  |
| `beneficiary.bankDetails.accountRoutingValue2` | string |  |
| `beneficiary.bankDetails.bankBranch` | string |  |
| `beneficiary.bankDetails.bankCountryCode` | string |  |
| `beneficiary.bankDetails.bankName` | string |  |
| `beneficiary.dateOfBirth` | date |  |
| `beneficiary.entityType` | string |  |
| `beneficiary.firstName` | string |  |
| `beneficiary.lastName` | string |  |
| `beneficiary.type` | string |  |
| `id` | string |  |
| `payerEntityType` | string |  |
| `transferMethods[]` | string |  |

## Native endpoint

Through the native Airwallex API, this operation is `GET /api/v1/beneficiaries` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-beneficiaries.md) for the provider-specific parameters and requirements.

