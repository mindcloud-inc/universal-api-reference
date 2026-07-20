# OneSuite: Create Company

Creates a company in OneSuite.

```
POST https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Acme Corporation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Acme Corporation"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Company name from the official OneSuite create-company docs. Example: `Acme Corporation`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityId` | string | no | Optional opportunity ID to connect when creating the company. Example: `cmjhopp000000000000001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountOwner": {},
      "accountOwnerId": {},
      "address1": "string",
      "address2": "string",
      "annualRecurringRevenue": 1,
      "bgColor": "string",
      "brandColour": "string",
      "businessId": "string",
      "city": "string",
      "country": "string",
      "countryCode": "string",
      "countryDialCode": "string",
      "countryFlag": "string",
      "createdAt": "string",
      "createdBy": {
        "user": {
          "fullName": "Ava Chen",
          "profileImg": {}
        }
      },
      "createdById": "string",
      "currency": "string",
      "currencyName": "Ava Chen",
      "currencySymbol": "string",
      "customSocialMediaUrl": "https://example.com",
      "employees": 1,
      "facebookUrl": "https://example.com",
      "fgColor": "string",
      "hiddenInCrm": true,
      "icp": true,
      "id": "string",
      "industry": {},
      "industryId": {},
      "instagramUrl": "https://example.com",
      "isClient": true,
      "linkedinUrl": "https://example.com",
      "logo": {},
      "name": "Ava Chen",
      "pointOfContactId": {},
      "source": {},
      "sourceId": {},
      "state": "string",
      "threadUrl": "https://example.com",
      "tiktokUrl": "https://example.com",
      "twitterUrl": "https://example.com",
      "updatedAt": "string",
      "youtubeUrl": "https://example.com",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountOwner` | object |  |
| `accountOwnerId` | object |  |
| `address1` | string |  |
| `address2` | string |  |
| `annualRecurringRevenue` | number |  |
| `bgColor` | string |  |
| `brandColour` | string |  |
| `businessId` | string |  |
| `city` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `countryDialCode` | string |  |
| `countryFlag` | string |  |
| `createdAt` | string |  |
| `createdBy.user.fullName` | string |  |
| `createdBy.user.profileImg` | object |  |
| `createdById` | string |  |
| `currency` | string |  |
| `currencyName` | string |  |
| `currencySymbol` | string |  |
| `customSocialMediaUrl` | string |  |
| `employees` | number |  |
| `facebookUrl` | string |  |
| `fgColor` | string |  |
| `hiddenInCrm` | boolean |  |
| `icp` | boolean |  |
| `id` | string |  |
| `industry` | object |  |
| `industryId` | object |  |
| `instagramUrl` | string |  |
| `isClient` | boolean |  |
| `linkedinUrl` | string |  |
| `logo` | object |  |
| `name` | string |  |
| `pointOfContactId` | object |  |
| `source` | object |  |
| `sourceId` | object |  |
| `state` | string |  |
| `threadUrl` | string |  |
| `tiktokUrl` | string |  |
| `twitterUrl` | string |  |
| `updatedAt` | string |  |
| `youtubeUrl` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `POST /v2/companies` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

