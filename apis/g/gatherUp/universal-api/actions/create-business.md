# GatherUp: Create Business

Creates a new business in GatherUp.

```
POST https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-business
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GatherUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-business" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessName": "Ava Chen",
  "businessType": "string",
  "city": "string",
  "country": "string",
  "phone": "string",
  "state": "string",
  "streetAddress": "string",
  "zip": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gatherUp/latest/actions/create-business', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessName": "Ava Chen",
    "businessType": "string",
    "city": "string",
    "country": "string",
    "phone": "string",
    "state": "string",
    "streetAddress": "string",
    "zip": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `businessName` | string | yes | Business name. |
| `businessOwnerAccount` | number | no | Set to 1 if you want to create business manager (aka User). |
| `businessOwnerEmail` | string | no | User email. |
| `businessOwnerFirstName` | string | no | User first name. |
| `businessOwnerLastName` | string | no | User last name. |
| `businessOwnerSendPasswordEmail` | number | no | Send email with password |
| `businessType` | string | yes | Google business type. |
| `city` | string | yes | Business city. |
| `country` | string | yes | Business country code or full name. |
| `customField` | string | no | Custom ID (whitelabeled accounts only). |
| `emailImage` | string | no | Email Picture. |
| `emailLogo` | string | no | Company Logo. |
| `feedbackBanner` | string | no | Feedback Page Banner. |
| `organisationType` | string | no | Organisation type: company, corporation, non profit, school, office, practice, agency, church,restaurant, event, firm, store, dealership |
| `phone` | string | yes | Mobile phone number. |
| `state` | string | yes | Business state code or full name. |
| `streetAddress` | string | yes | Business street address. |
| `websiteUrl` | string | no | Business website url. |
| `zip` | string | yes | Business zip code. |
| `language` | string | no | Business language |

## Response

```json
{
  "success": true,
  "data": [
    {
      "businessId": 1,
      "businessManagerId": 1,
      "businessOwnerErrorCode": 1,
      "businessOwnerErrorMessage": "string",
      "businessOwnerPassword": "string",
      "errorCode": 1,
      "errorMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `businessId` | number |  |
| `businessManagerId` | number |  |
| `businessOwnerErrorCode` | number |  |
| `businessOwnerErrorMessage` | string |  |
| `businessOwnerPassword` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |

## Native endpoint

Through the native GatherUp API, this operation is `POST /business/create` (base URL `https://app.gatherup.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-business.md) for the provider-specific parameters and requirements.

