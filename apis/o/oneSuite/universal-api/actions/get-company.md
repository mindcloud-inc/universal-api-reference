# OneSuite: Get Company

Retrieves a company from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-company?connectionId=$CONNECTION_ID&companyId=cmo7gu3gq02robo05g27zy4n0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "cmo7gu3gq02robo05g27zy4n0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-company?${params}`, {
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
| `companyId` | string | yes | Company ID from the OneSuite single-company docs. Example: `cmo7gu3gq02robo05g27zy4n0`. |

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
          "bgColor": "string",
          "businessId": "string",
          "closeDate": {},
          "companyId": "string",
          "createdAt": "string",
          "createdBy": {
            "id": "string",
            "user": {
              "email": "ava@example.com",
              "fullName": "Ava Chen",
              "id": "string",
              "profileImg": {}
            }
          },
          "createdById": "string",
          "currency": "string",
          "currencyName": "Ava Chen",
          "currencySymbol": "string",
          "fgColor": "string",
          "id": "string",
          "industryId": {},
          "name": "Ava Chen",
          "pointOfContact": {},
          "pointOfContactId": {},
          "position": 1,
          "sourceId": {},
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
          },
          "stageId": "string",
          "updatedAt": "string"
        }
      ],
      "pointOfContact": {
        "invitationStatus": "string"
      },
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
| `opportunities[].bgColor` | string |  |
| `opportunities[].businessId` | string |  |
| `opportunities[].closeDate` | object |  |
| `opportunities[].companyId` | string |  |
| `opportunities[].createdAt` | string |  |
| `opportunities[].createdBy.id` | string |  |
| `opportunities[].createdBy.user.email` | string |  |
| `opportunities[].createdBy.user.fullName` | string |  |
| `opportunities[].createdBy.user.id` | string |  |
| `opportunities[].createdBy.user.profileImg` | object |  |
| `opportunities[].createdById` | string |  |
| `opportunities[].currency` | string |  |
| `opportunities[].currencyName` | string |  |
| `opportunities[].currencySymbol` | string |  |
| `opportunities[].fgColor` | string |  |
| `opportunities[].id` | string |  |
| `opportunities[].industryId` | object |  |
| `opportunities[].name` | string |  |
| `opportunities[].pointOfContact` | object |  |
| `opportunities[].pointOfContactId` | object |  |
| `opportunities[].position` | number |  |
| `opportunities[].sourceId` | object |  |
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
| `opportunities[].stageId` | string |  |
| `opportunities[].updatedAt` | string |  |
| `pointOfContact.invitationStatus` | string |  |
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

Through the native OneSuite API, this operation is `GET /v1/companies/:company_id` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

