# Pinch Payments Universal API Examples

These examples use the MindCloud API key and Pinch Payments connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Merchant

Retrieves your merchant details from Pinch Payments.

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

Example response:

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

See the full [Get Merchant action reference](actions/get-merchant.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinchPayments/latest/actions/get-merchant).

## Create or Update Payer

Creates or updates a payer in Pinch Payments.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "ava@example.com",
  "firstName": "Ava"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-or-update-payer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "ava@example.com",
    "firstName": "Ava"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "agreements": [
        {}
      ],
      "companyName": "Ava Chen",
      "companyRegistrationNumber": "string",
      "country": "string",
      "countryCode": "string",
      "emailAddress": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "metadata": "string",
      "mobileNumber": "string",
      "postcode": "string",
      "sources": [
        {}
      ],
      "state": "string",
      "streetAddress": "string",
      "suburb": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create or Update Payer action reference](actions/create-or-update-payer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pinchPayments/latest/actions/create-or-update-payer).
