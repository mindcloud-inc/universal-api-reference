# OneSuite: Get Client

Retrieves a client from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-client?connectionId=$CONNECTION_ID&clientId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/get-client?${params}`, {
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
| `clientId` | string | yes | The ID of the client to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountOwner": {},
      "address1": "string",
      "address2": "string",
      "annualRecurringRevenue": 1,
      "assignedTo": {},
      "bgColor": "string",
      "city": "string",
      "companyId": "string",
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
      "currency": "string",
      "currencyName": "Ava Chen",
      "currencySymbol": "string",
      "customSocialMediaUrl": "https://example.com",
      "employees": 1,
      "facebookUrl": "https://example.com",
      "fgColor": "string",
      "icp": true,
      "id": "string",
      "industry": {},
      "instagramUrl": "https://example.com",
      "invitationStatus": "string",
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
      "peopleId": {},
      "pointOfContact": {
        "invitationStatus": "string"
      },
      "priority": {
        "bgColor": "string",
        "borderColor": "string",
        "businessId": "string",
        "createdAt": "string",
        "fgColor": "string",
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "slug": "string",
        "updatedAt": "string"
      },
      "priorityId": "string",
      "source": {},
      "state": "string",
      "status": {
        "bgColor": "string",
        "borderColor": "string",
        "businessId": "string",
        "createdAt": "string",
        "fgColor": "string",
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "slug": "string",
        "updatedAt": "string"
      },
      "statusId": "string",
      "threadUrl": "https://example.com",
      "tiktokUrl": "https://example.com",
      "twitterUrl": "https://example.com",
      "type": "string",
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
| `address1` | string |  |
| `address2` | string |  |
| `annualRecurringRevenue` | number |  |
| `assignedTo` | object |  |
| `bgColor` | string |  |
| `city` | string |  |
| `companyId` | string |  |
| `country` | string |  |
| `countryCode` | string |  |
| `countryDialCode` | string |  |
| `countryFlag` | string |  |
| `createdAt` | string |  |
| `createdBy.user.fullName` | string |  |
| `createdBy.user.profileImg` | object |  |
| `currency` | string |  |
| `currencyName` | string |  |
| `currencySymbol` | string |  |
| `customSocialMediaUrl` | string |  |
| `employees` | number |  |
| `facebookUrl` | string |  |
| `fgColor` | string |  |
| `icp` | boolean |  |
| `id` | string |  |
| `industry` | object |  |
| `instagramUrl` | string |  |
| `invitationStatus` | string |  |
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
| `peopleId` | object |  |
| `pointOfContact.invitationStatus` | string |  |
| `priority.bgColor` | string |  |
| `priority.borderColor` | string |  |
| `priority.businessId` | string |  |
| `priority.createdAt` | string |  |
| `priority.fgColor` | string |  |
| `priority.id` | string |  |
| `priority.isDefault` | boolean |  |
| `priority.name` | string |  |
| `priority.slug` | string |  |
| `priority.updatedAt` | string |  |
| `priorityId` | string |  |
| `source` | object |  |
| `state` | string |  |
| `status.bgColor` | string |  |
| `status.borderColor` | string |  |
| `status.businessId` | string |  |
| `status.createdAt` | string |  |
| `status.fgColor` | string |  |
| `status.id` | string |  |
| `status.isDefault` | boolean |  |
| `status.name` | string |  |
| `status.slug` | string |  |
| `status.updatedAt` | string |  |
| `statusId` | string |  |
| `threadUrl` | string |  |
| `tiktokUrl` | string |  |
| `twitterUrl` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `youtubeUrl` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/clients/:client_id` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

