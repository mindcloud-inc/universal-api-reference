# Finmo: List Payout Beneficiaries

Retrieves payout beneficiaries from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payout-beneficiaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payout-beneficiaries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payout-beneficiaries?${params}`, {
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
| `type` | string | no |  |
| `includeDeleted` | boolean | no |  |
| `createdAt` | string | no |  |
| `startTime` | number | no |  |
| `endTime` | number | no |  |
| `limit` | number | no |  |
| `page` | number | no |  |

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
| `data[].aba` | object |  |
| `data[].accountNumber` | string |  |
| `data[].accountType` | object |  |
| `data[].additionalData` | object |  |
| `data[].bankCity` | object |  |
| `data[].bankCode` | object |  |
| `data[].bankCountry` | object |  |
| `data[].bankName` | object |  |
| `data[].bankState` | object |  |
| `data[].beneficiaryName` | string |  |
| `data[].bicSwift` | object |  |
| `data[].billerCode` | object |  |
| `data[].branchCode` | object |  |
| `data[].bsb` | string |  |
| `data[].createdAt` | string |  |
| `data[].createdBy` | string |  |
| `data[].currency` | string |  |
| `data[].customerReferenceNumber` | object |  |
| `data[].description` | string |  |
| `data[].duitnowProxyType` | object |  |
| `data[].duitnowProxyValue` | object |  |
| `data[].fpsProxyType` | object |  |
| `data[].fpsProxyValue` | object |  |
| `data[].iban` | object |  |
| `data[].ifsc` | object |  |
| `data[].individual` | object |  |
| `data[].individual.addressCity` | object |  |
| `data[].individual.addressCountry` | object |  |
| `data[].individual.addressLine1` | object |  |
| `data[].individual.addressLine2` | object |  |
| `data[].individual.addressState` | object |  |
| `data[].individual.addressZipCode` | object |  |
| `data[].individual.countryOfResidence` | object |  |
| `data[].individual.dob` | object |  |
| `data[].individual.email` | object |  |
| `data[].individual.firstName` | string |  |
| `data[].individual.identificationCustomType` | object |  |
| `data[].individual.identificationType` | object |  |
| `data[].individual.identificationValue` | object |  |
| `data[].individual.lastName` | string |  |
| `data[].individual.nationality` | object |  |
| `data[].individual.phoneCountryCode` | object |  |
| `data[].individual.phoneNumber` | object |  |
| `data[].individual.phoneNumberE164` | object |  |
| `data[].individual.registrationNumber` | object |  |
| `data[].interacEmail` | object |  |
| `data[].intermediaryBicSwift` | object |  |
| `data[].isActive` | boolean |  |
| `data[].metadata` | object |  |
| `data[].metadata.source` | string |  |
| `data[].metadata.testRun` | string |  |
| `data[].nickname` | object |  |
| `data[].organizationReferenceId` | string |  |
| `data[].orgId` | string |  |
| `data[].payId` | object |  |
| `data[].payIdType` | object |  |
| `data[].payoutBeneficiaryId` | string |  |
| `data[].proxyType` | object |  |
| `data[].proxyValue` | object |  |
| `data[].sortCode` | object |  |
| `data[].tagIdList` | object |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `data[].upiId` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /payout-beneficiary` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payout-beneficiaries.md) for the provider-specific parameters and requirements.

