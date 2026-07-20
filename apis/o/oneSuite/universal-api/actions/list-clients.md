# OneSuite: List Clients

Retrieves clients from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-clients?${params}`, {
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
      "clients": [
        {
          "accountOwner": {},
          "accountOwnerId": {},
          "address1": "string",
          "address2": "string",
          "annualRecurringRevenue": 1,
          "assignedTo": {},
          "bgColor": "string",
          "brandColour": "string",
          "businessId": "string",
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
          "createdById": "string",
          "currency": "string",
          "currencyName": "Ava Chen",
          "currencySymbol": "string",
          "customSocialMediaUrl": "https://example.com",
          "employees": 1,
          "facebookUrl": "https://example.com",
          "fgColor": "string",
          "hasPortalAccess": true,
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
          "peopleId": {},
          "pointOfContact": {},
          "pointOfContactId": {},
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
          "sourceId": {},
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clients[].accountOwner` | object |  |
| `clients[].accountOwnerId` | object |  |
| `clients[].address1` | string |  |
| `clients[].address2` | string |  |
| `clients[].annualRecurringRevenue` | number |  |
| `clients[].assignedTo` | object |  |
| `clients[].bgColor` | string |  |
| `clients[].brandColour` | string |  |
| `clients[].businessId` | string |  |
| `clients[].city` | string |  |
| `clients[].companyId` | string |  |
| `clients[].country` | string |  |
| `clients[].countryCode` | string |  |
| `clients[].countryDialCode` | string |  |
| `clients[].countryFlag` | string |  |
| `clients[].createdAt` | string |  |
| `clients[].createdBy.user.fullName` | string |  |
| `clients[].createdBy.user.profileImg` | object |  |
| `clients[].createdById` | string |  |
| `clients[].currency` | string |  |
| `clients[].currencyName` | string |  |
| `clients[].currencySymbol` | string |  |
| `clients[].customSocialMediaUrl` | string |  |
| `clients[].employees` | number |  |
| `clients[].facebookUrl` | string |  |
| `clients[].fgColor` | string |  |
| `clients[].hasPortalAccess` | boolean |  |
| `clients[].hiddenInCrm` | boolean |  |
| `clients[].icp` | boolean |  |
| `clients[].id` | string |  |
| `clients[].industry` | object |  |
| `clients[].industryId` | object |  |
| `clients[].instagramUrl` | string |  |
| `clients[].isClient` | boolean |  |
| `clients[].linkedinUrl` | string |  |
| `clients[].logo` | object |  |
| `clients[].name` | string |  |
| `clients[].peopleId` | object |  |
| `clients[].pointOfContact` | object |  |
| `clients[].pointOfContactId` | object |  |
| `clients[].priority.bgColor` | string |  |
| `clients[].priority.borderColor` | string |  |
| `clients[].priority.businessId` | string |  |
| `clients[].priority.createdAt` | string |  |
| `clients[].priority.fgColor` | string |  |
| `clients[].priority.id` | string |  |
| `clients[].priority.isDefault` | boolean |  |
| `clients[].priority.name` | string |  |
| `clients[].priority.slug` | string |  |
| `clients[].priority.updatedAt` | string |  |
| `clients[].priorityId` | string |  |
| `clients[].source` | object |  |
| `clients[].sourceId` | object |  |
| `clients[].state` | string |  |
| `clients[].status.bgColor` | string |  |
| `clients[].status.borderColor` | string |  |
| `clients[].status.businessId` | string |  |
| `clients[].status.createdAt` | string |  |
| `clients[].status.fgColor` | string |  |
| `clients[].status.id` | string |  |
| `clients[].status.isDefault` | boolean |  |
| `clients[].status.name` | string |  |
| `clients[].status.slug` | string |  |
| `clients[].status.updatedAt` | string |  |
| `clients[].statusId` | string |  |
| `clients[].threadUrl` | string |  |
| `clients[].tiktokUrl` | string |  |
| `clients[].twitterUrl` | string |  |
| `clients[].type` | string |  |
| `clients[].updatedAt` | string |  |
| `clients[].youtubeUrl` | string |  |
| `clients[].zip` | string |  |
| `message` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/clients` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

