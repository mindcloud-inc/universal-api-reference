# Finmo: List Customers

Retrieves customers from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-customers?${params}`, {
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
| `type` | string | no | Filter customers by type. |
| `createdAt` | string | no | Filter by UTC creation date (YYYY-MM-DD). |
| `includeDeleted` | boolean | no | Include deleted customers in the results. |
| `startTime` | number | no | Filter from epoch start timestamp. |
| `endTime` | number | no | Filter to epoch end timestamp. |
| `limit` | number | no | Maximum number of records per page. |
| `page` | number | no | Page number to return. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `data[].accountUsagePurpose` | string |  |
| `data[].companyDomain` | object |  |
| `data[].createdAt` | string |  |
| `data[].createdBy` | string |  |
| `data[].customerHostedUrl` | object |  |
| `data[].customerId` | string |  |
| `data[].description` | string |  |
| `data[].gcaActivatedAt` | object |  |
| `data[].gcaActivationStatus` | string |  |
| `data[].individual` | object |  |
| `data[].individual.addressCity` | object |  |
| `data[].individual.addressCountry` | object |  |
| `data[].individual.addressLine1` | object |  |
| `data[].individual.addressLine2` | object |  |
| `data[].individual.addressProofDocumentId` | object |  |
| `data[].individual.addressState` | object |  |
| `data[].individual.addressZipCode` | object |  |
| `data[].individual.countryOfResidence` | object |  |
| `data[].individual.dob` | object |  |
| `data[].individual.email` | object |  |
| `data[].individual.firstName` | string |  |
| `data[].individual.identificationCustomType` | object |  |
| `data[].individual.identificationDocumentId` | object |  |
| `data[].individual.identificationType` | object |  |
| `data[].individual.identificationValue` | object |  |
| `data[].individual.lastName` | string |  |
| `data[].individual.nationality` | object |  |
| `data[].individual.phoneCountryCode` | object |  |
| `data[].individual.phoneNumber` | object |  |
| `data[].individual.phoneNumberE164` | object |  |
| `data[].isActive` | boolean |  |
| `data[].isEnabled` | boolean |  |
| `data[].isGcaEnabled` | boolean |  |
| `data[].isSenderValidationEnabled` | boolean |  |
| `data[].isUrlExpired` | boolean |  |
| `data[].isWalletReady` | boolean |  |
| `data[].metadata` | object |  |
| `data[].metadata.source` | string |  |
| `data[].metadata.testRun` | string |  |
| `data[].organizationReferenceId` | string |  |
| `data[].orgId` | string |  |
| `data[].payinSenderIdList` | object |  |
| `data[].status` | string |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `data[].webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /customer` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

