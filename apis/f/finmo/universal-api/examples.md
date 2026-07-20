# Finmo Universal API Examples

These examples use the MindCloud API key and Finmo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Wallets

Retrieves wallets from the Finmo platform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-wallets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-wallets?${params}`, {
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
      "data": [
        [
          {}
        ]
      ],
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

See the full [List Wallets action reference](actions/list-wallets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finmo/latest/actions/list-wallets).

## Create Customer

Creates a new customer in Finmo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "accountUsagePurpose": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "accountUsagePurpose": "string"
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
      "data": {
        "accountUsagePurpose": "string",
        "companyDomain": {},
        "createdAt": "string",
        "createdBy": "string",
        "customerHostedUrl": {},
        "customerId": "string",
        "description": "string",
        "gcaActivatedAt": {},
        "gcaActivationStatus": "string",
        "individual": {
          "addressCity": {},
          "addressCountry": {},
          "addressLine1": {},
          "addressLine2": {},
          "addressProofDocumentId": {},
          "addressState": {},
          "addressZipCode": {},
          "countryOfResidence": {},
          "dob": {},
          "email": {},
          "firstName": "Ava",
          "identificationCustomType": {},
          "identificationDocumentId": {},
          "identificationType": {},
          "identificationValue": {},
          "lastName": "Chen",
          "nationality": {},
          "phoneCountryCode": {},
          "phoneNumber": {},
          "phoneNumberE164": {}
        },
        "isActive": true,
        "isEnabled": true,
        "isGcaEnabled": true,
        "isSenderValidationEnabled": true,
        "isUrlExpired": true,
        "isWalletReady": true,
        "metadata": {
          "source": "string",
          "testRun": "string"
        },
        "organizationReferenceId": "string",
        "orgId": "string",
        "payinSenderIdList": {},
        "status": "string",
        "type": "string",
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

See the full [Create Customer action reference](actions/create-customer.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/finmo/latest/actions/create-customer).
