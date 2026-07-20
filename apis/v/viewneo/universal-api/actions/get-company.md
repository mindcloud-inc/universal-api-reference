# Viewneo: Get Company

Retrieves the current company details from Viewneo.

```
GET https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-company?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/get-company?${params}`, {
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
      "alltronReseller": {},
      "branch": 1,
      "brandCompanyId": {},
      "city": "string",
      "country": "string",
      "createdAt": "string",
      "customDunning": 1,
      "customLicencePrice": {},
      "deletedAt": {},
      "deletesAt": {},
      "description": {},
      "discountValue": {},
      "expiresAt": {},
      "geoLocation": "string",
      "id": 1,
      "isAnalyticsEnabled": {},
      "isBrand": 1,
      "isDiniopayEnabled": 1,
      "isLocked": 1,
      "isPartner": 1,
      "isTrial": 1,
      "lastLoginAt": "string",
      "maxAmountCustomLicencePrice": {},
      "microsoftFaceApiKey": {},
      "microsoftFaceApiUrl": {},
      "name": "Ava Chen",
      "parentId": {},
      "partnerId": {},
      "postalCode": "string",
      "priceAdjustment": 1,
      "registrationType": 1,
      "stage": {},
      "state": "string",
      "street": "string",
      "streetNumber": "string",
      "stripeCustomerId": {},
      "subName": "Ava Chen",
      "totalLicences": "string",
      "totalStorage": {},
      "totalSubAccounts": 1,
      "type": 1,
      "updatedAt": "string",
      "userIdAsPartner": {},
      "vat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alltronReseller` | object |  |
| `branch` | number |  |
| `brandCompanyId` | object |  |
| `city` | string |  |
| `country` | string |  |
| `createdAt` | string |  |
| `customDunning` | number |  |
| `customLicencePrice` | object |  |
| `deletedAt` | object |  |
| `deletesAt` | object |  |
| `description` | object |  |
| `discountValue` | object |  |
| `expiresAt` | object |  |
| `geoLocation` | string |  |
| `id` | number |  |
| `isAnalyticsEnabled` | object |  |
| `isBrand` | number |  |
| `isDiniopayEnabled` | number |  |
| `isLocked` | number |  |
| `isPartner` | number |  |
| `isTrial` | number |  |
| `lastLoginAt` | string |  |
| `maxAmountCustomLicencePrice` | object |  |
| `microsoftFaceApiKey` | object |  |
| `microsoftFaceApiUrl` | object |  |
| `name` | string |  |
| `parentId` | object |  |
| `partnerId` | object |  |
| `postalCode` | string |  |
| `priceAdjustment` | number |  |
| `registrationType` | number |  |
| `stage` | object |  |
| `state` | string |  |
| `street` | string |  |
| `streetNumber` | string |  |
| `stripeCustomerId` | object |  |
| `subName` | string |  |
| `totalLicences` | string |  |
| `totalStorage` | object |  |
| `totalSubAccounts` | number |  |
| `type` | number |  |
| `updatedAt` | string |  |
| `userIdAsPartner` | object |  |
| `vat` | string |  |

## Native endpoint

Through the native Viewneo API, this operation is `GET /company` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

