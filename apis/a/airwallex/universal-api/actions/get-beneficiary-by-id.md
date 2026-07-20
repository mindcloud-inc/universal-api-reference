# Airwallex: Get Beneficiary by ID

Retrieves a beneficiary by ID from Airwallex.

```
GET https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-beneficiary-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airwallex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-beneficiary-by-id?connectionId=$CONNECTION_ID&beneficiaryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "beneficiaryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airwallex/latest/actions/get-beneficiary-by-id?${params}`, {
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
| `beneficiaryId` | string | yes | The Airwallex beneficiary ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `beneficiary.firstName` | string |  |
| `beneficiary.lastName` | string |  |
| `beneficiary.type` | string |  |
| `id` | string |  |
| `payerEntityType` | string |  |
| `transferMethods[]` | string |  |

## Native endpoint

Through the native Airwallex API, this operation is `GET /api/v1/beneficiaries/{{beneficiaryId}}` (base URL `https://api-demo.airwallex.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-beneficiary-by-id.md) for the provider-specific parameters and requirements.

