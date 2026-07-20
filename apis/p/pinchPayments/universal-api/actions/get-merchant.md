# Pinch Payments: Get Merchant

Retrieves your merchant details from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-merchant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-merchant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-merchant?${params}`, {
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
      "bankStatementLabel": "string",
      "companyEmail": "ava@example.com",
      "companyName": "Ava Chen",
      "companyPhone": "string",
      "companyRegistrationNumber": "string",
      "companyWebsiteUrl": "https://example.com",
      "compliance": {
        "bankAccountVerificationStatus": "string",
        "contactComplianceResponses": [
          {
            "contactId": "string",
            "documentVerificationStatus": "string",
            "emailVerificationStatus": "ava@example.com",
            "identityVerificationStatus": "string",
            "overallStatus": "string",
            "phoneVerificationStatus": "string"
          }
        ],
        "documentVerificationStatus": "string",
        "entityDetailsVerificationStatus": "string",
        "liveEnabled": true,
        "merchantNotes": "string",
        "settlementsEnabled": true,
        "status": "string",
        "submissionDate": "2026-05-07T12:00:00.000Z",
        "submissionStatus": "string",
        "transactionsEnabled": true
      },
      "contacts": [
        {
          "contactType": "string",
          "country": "string",
          "dob": "2026-05-07T12:00:00.000Z",
          "driversLicenseSupplied": true,
          "email": "ava@example.com",
          "firstName": "Ava",
          "fullName": "Ava Chen",
          "governmentNumberSupplied": true,
          "id": "string",
          "isPrimaryContact": true,
          "isUbo": true,
          "lastName": "Chen",
          "passportNumberSupplied": true,
          "phone": "string"
        }
      ],
      "country": "string",
      "createdDateUtc": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "legalCountry": "string",
      "legalEntityName": "Ava Chen",
      "legalPostcode": "string",
      "legalState": "string",
      "legalStreetAddress": "string",
      "legalSuburb": "string",
      "livePublishableKey": "string",
      "mastercardDpaId": "string",
      "merchantIdentifiers": [
        {
          "identityProvider": "string",
          "merchantIdentifier": "string"
        }
      ],
      "natureOfBusiness": "string",
      "organisationType": "string",
      "postcode": "string",
      "state": "string",
      "streetAddress": "string",
      "suburb": "string",
      "testMerchantId": "string",
      "testOnlyMerchant": true,
      "testPublishableKey": "string",
      "timeZone": "string",
      "tradingCountry": "string",
      "tradingPostcode": "string",
      "tradingState": "string",
      "tradingStreetAddress": "string",
      "tradingSuburb": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bankStatementLabel` | string |  |
| `companyEmail` | string |  |
| `companyName` | string |  |
| `companyPhone` | string |  |
| `companyRegistrationNumber` | string |  |
| `companyWebsiteUrl` | string |  |
| `compliance.bankAccountVerificationStatus` | string |  |
| `compliance.contactComplianceResponses[].contactId` | string |  |
| `compliance.contactComplianceResponses[].documentVerificationStatus` | string |  |
| `compliance.contactComplianceResponses[].emailVerificationStatus` | string |  |
| `compliance.contactComplianceResponses[].identityVerificationStatus` | string |  |
| `compliance.contactComplianceResponses[].overallStatus` | string |  |
| `compliance.contactComplianceResponses[].phoneVerificationStatus` | string |  |
| `compliance.documentVerificationStatus` | string |  |
| `compliance.entityDetailsVerificationStatus` | string |  |
| `compliance.liveEnabled` | boolean |  |
| `compliance.merchantNotes` | string |  |
| `compliance.settlementsEnabled` | boolean |  |
| `compliance.status` | string |  |
| `compliance.submissionDate` | date |  |
| `compliance.submissionStatus` | string |  |
| `compliance.transactionsEnabled` | boolean |  |
| `contacts[].contactType` | string |  |
| `contacts[].country` | string |  |
| `contacts[].dob` | date |  |
| `contacts[].driversLicenseSupplied` | boolean |  |
| `contacts[].email` | string |  |
| `contacts[].firstName` | string |  |
| `contacts[].fullName` | string |  |
| `contacts[].governmentNumberSupplied` | boolean |  |
| `contacts[].id` | string |  |
| `contacts[].isPrimaryContact` | boolean |  |
| `contacts[].isUbo` | boolean |  |
| `contacts[].lastName` | string |  |
| `contacts[].passportNumberSupplied` | boolean |  |
| `contacts[].phone` | string |  |
| `country` | string |  |
| `createdDateUtc` | date |  |
| `id` | string |  |
| `legalCountry` | string |  |
| `legalEntityName` | string |  |
| `legalPostcode` | string |  |
| `legalState` | string |  |
| `legalStreetAddress` | string |  |
| `legalSuburb` | string |  |
| `livePublishableKey` | string |  |
| `mastercardDpaId` | string |  |
| `merchantIdentifiers[].identityProvider` | string |  |
| `merchantIdentifiers[].merchantIdentifier` | string |  |
| `natureOfBusiness` | string |  |
| `organisationType` | string |  |
| `postcode` | string |  |
| `state` | string |  |
| `streetAddress` | string |  |
| `suburb` | string |  |
| `testMerchantId` | string |  |
| `testOnlyMerchant` | boolean |  |
| `testPublishableKey` | string |  |
| `timeZone` | string |  |
| `tradingCountry` | string |  |
| `tradingPostcode` | string |  |
| `tradingState` | string |  |
| `tradingStreetAddress` | string |  |
| `tradingSuburb` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /merchants` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-merchant.md) for the provider-specific parameters and requirements.

