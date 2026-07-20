# Finmo: Create Customer

Creates a new customer in Finmo.

```
POST https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Description about the customer. |
| `type` | string | yes | Customer type: company or individual. |
| `organizationReferenceId` | string | no | Organization reference identifier for the customer. |
| `metadata` | object | no | Custom metadata object. |
| `accountUsagePurpose` | string | yes | Purpose of opening the account. |
| `company` | object | no | Company payload when the customer type is company. |
| `individual` | object | no | Individual payload when the customer type is individual. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.accountUsagePurpose` | string |  |
| `data.companyDomain` | object |  |
| `data.createdAt` | string |  |
| `data.createdBy` | string |  |
| `data.customerHostedUrl` | object |  |
| `data.customerId` | string |  |
| `data.description` | string |  |
| `data.gcaActivatedAt` | object |  |
| `data.gcaActivationStatus` | string |  |
| `data.individual` | object |  |
| `data.individual.addressCity` | object |  |
| `data.individual.addressCountry` | object |  |
| `data.individual.addressLine1` | object |  |
| `data.individual.addressLine2` | object |  |
| `data.individual.addressProofDocumentId` | object |  |
| `data.individual.addressState` | object |  |
| `data.individual.addressZipCode` | object |  |
| `data.individual.countryOfResidence` | object |  |
| `data.individual.dob` | object |  |
| `data.individual.email` | object |  |
| `data.individual.firstName` | string |  |
| `data.individual.identificationCustomType` | object |  |
| `data.individual.identificationDocumentId` | object |  |
| `data.individual.identificationType` | object |  |
| `data.individual.identificationValue` | object |  |
| `data.individual.lastName` | string |  |
| `data.individual.nationality` | object |  |
| `data.individual.phoneCountryCode` | object |  |
| `data.individual.phoneNumber` | object |  |
| `data.individual.phoneNumberE164` | object |  |
| `data.isActive` | boolean |  |
| `data.isEnabled` | boolean |  |
| `data.isGcaEnabled` | boolean |  |
| `data.isSenderValidationEnabled` | boolean |  |
| `data.isUrlExpired` | boolean |  |
| `data.isWalletReady` | boolean |  |
| `data.metadata` | object |  |
| `data.metadata.source` | string |  |
| `data.metadata.testRun` | string |  |
| `data.organizationReferenceId` | string |  |
| `data.orgId` | string |  |
| `data.payinSenderIdList` | object |  |
| `data.status` | string |  |
| `data.type` | string |  |
| `data.updatedAt` | string |  |
| `data.webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `POST /customer` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

