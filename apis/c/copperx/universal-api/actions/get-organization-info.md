# Copperx: Get Organization Info

Retrieves organization record details from Copperx.

```
GET https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-organization-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Copperx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-organization-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/copperx/latest/actions/get-organization-info?${params}`, {
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
      "addressDetails": {},
      "addresses": [
        {}
      ],
      "brandColor": "string",
      "brandLogo": "string",
      "companyIdentificationNumber": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "featureAccessRequests": [
        {}
      ],
      "id": "string",
      "monthlyPaymentVolume": "string",
      "name": "Ava Chen",
      "noOfEmployees": 1,
      "ownerId": "string",
      "phone": "string",
      "privacyUrl": "https://example.com",
      "referralCode": "string",
      "referrerId": "string",
      "status": "string",
      "supportEmail": "ava@example.com",
      "supportUrl": "https://example.com",
      "taxIdentificationNumber": "string",
      "termsUrl": "https://example.com",
      "type": "string",
      "updatedAt": "string",
      "websiteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressDetails` | object |  |
| `addresses` | array<object> |  |
| `brandColor` | string |  |
| `brandLogo` | string |  |
| `companyIdentificationNumber` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `featureAccessRequests` | array<object> |  |
| `id` | string |  |
| `monthlyPaymentVolume` | string |  |
| `name` | string |  |
| `noOfEmployees` | number |  |
| `ownerId` | string |  |
| `phone` | string |  |
| `privacyUrl` | string |  |
| `referralCode` | string |  |
| `referrerId` | string |  |
| `status` | string |  |
| `supportEmail` | string |  |
| `supportUrl` | string |  |
| `taxIdentificationNumber` | string |  |
| `termsUrl` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `websiteUrl` | string |  |

## Native endpoint

Through the native Copperx API, this operation is `GET /organization` (base URL `https://api.copperx.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-info.md) for the provider-specific parameters and requirements.

