# Finmo: Update Customer

Updates an existing customer in Finmo.

```
PUT https://connect.mindcloud.co/v1/universal/finmo/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "type": "string",
  "accountUsagePurpose": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
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
| `customerId` | string | yes | Customer identifier to update. |
| `description` | string | no | Description about the customer. |
| `type` | string | yes | Customer type: company or individual. |
| `organizationReferenceId` | string | no | Organization reference identifier for the customer. |
| `isEnabled` | boolean | no | Flag to enable or disable the customer. |
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
          "addressCity": "string",
          "addressCountry": "string",
          "addressLine1": "string",
          "addressLine2": {},
          "addressProofDocumentId": "string",
          "addressState": "string",
          "addressZipCode": "string",
          "countryOfResidence": "string",
          "dob": "string",
          "email": "ava@example.com",
          "firstName": "Ava",
          "identificationCustomType": {},
          "identificationDocumentId": "string",
          "identificationType": "string",
          "identificationValue": "string",
          "lastName": "Chen",
          "nationality": "string",
          "phoneCountryCode": "string",
          "phoneNumber": "string",
          "phoneNumberE164": "string"
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
| `data.individual.addressCity` | string |  |
| `data.individual.addressCountry` | string |  |
| `data.individual.addressLine1` | string |  |
| `data.individual.addressLine2` | object |  |
| `data.individual.addressProofDocumentId` | string |  |
| `data.individual.addressState` | string |  |
| `data.individual.addressZipCode` | string |  |
| `data.individual.countryOfResidence` | string |  |
| `data.individual.dob` | string |  |
| `data.individual.email` | string |  |
| `data.individual.firstName` | string |  |
| `data.individual.identificationCustomType` | object |  |
| `data.individual.identificationDocumentId` | string |  |
| `data.individual.identificationType` | string |  |
| `data.individual.identificationValue` | string |  |
| `data.individual.lastName` | string |  |
| `data.individual.nationality` | string |  |
| `data.individual.phoneCountryCode` | string |  |
| `data.individual.phoneNumber` | string |  |
| `data.individual.phoneNumberE164` | string |  |
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

Through the native Finmo API, this operation is `PATCH /customer/:customer_id` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

