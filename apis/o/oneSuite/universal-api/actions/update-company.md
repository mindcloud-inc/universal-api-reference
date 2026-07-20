# OneSuite: Update Company

Updates a company in OneSuite.

```
PUT https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "cmo7gu3gq02robo05g27zy4n0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "cmo7gu3gq02robo05g27zy4n0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | yes | Company ID from the OneSuite update-company docs. Example: `cmo7gu3gq02robo05g27zy4n0`. |
| `name` | string | no | Updated company name. Example: `Codex QA Company Updated`. |

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
      "opportunities": [
        {
          "amount": 1,
          "closeDate": {},
          "id": "string",
          "name": "Ava Chen",
          "stage": {
            "bgColor": "string",
            "borderColor": "string",
            "businessId": "string",
            "createdAt": "string",
            "darkColor": "string",
            "fgColor": "string",
            "id": "string",
            "isDefault": true,
            "isFolded": true,
            "lightColor": "string",
            "name": "Ava Chen",
            "sortId": 1,
            "updatedAt": "string"
          }
        }
      ],
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
| `opportunities[].amount` | number |  |
| `opportunities[].closeDate` | object |  |
| `opportunities[].id` | string |  |
| `opportunities[].name` | string |  |
| `opportunities[].stage.bgColor` | string |  |
| `opportunities[].stage.borderColor` | string |  |
| `opportunities[].stage.businessId` | string |  |
| `opportunities[].stage.createdAt` | string |  |
| `opportunities[].stage.darkColor` | string |  |
| `opportunities[].stage.fgColor` | string |  |
| `opportunities[].stage.id` | string |  |
| `opportunities[].stage.isDefault` | boolean |  |
| `opportunities[].stage.isFolded` | boolean |  |
| `opportunities[].stage.lightColor` | string |  |
| `opportunities[].stage.name` | string |  |
| `opportunities[].stage.sortId` | number |  |
| `opportunities[].stage.updatedAt` | string |  |
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

Through the native OneSuite API, this operation is `PATCH /v2/companies/:company_id` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-company.md) for the provider-specific parameters and requirements.

