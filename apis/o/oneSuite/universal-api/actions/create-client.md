# OneSuite: Create Client

Creates a client in OneSuite.

```
POST https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "0",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "0",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | yes | Type of client: company or individual One of: `0`, `1`. |
| `name` | string | yes | Client name |

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

Through the native OneSuite API, this operation is `POST /v2/clients` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

