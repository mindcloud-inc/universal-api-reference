# OneSuite: List People

Retrieves people from OneSuite.

```
GET https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-people?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/list-people?${params}`, {
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
      "address1": "string",
      "address2": "string",
      "avatar": {},
      "bgColor": "string",
      "brandColour": "string",
      "businessId": "string",
      "city": "string",
      "clientId": {},
      "company": {},
      "companyId": {},
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
      "customSocialMediaUrl": "https://example.com",
      "facebookUrl": "https://example.com",
      "fgColor": "string",
      "hiddenInCrm": true,
      "id": "string",
      "industry": {},
      "industryId": {},
      "instagramUrl": "https://example.com",
      "invitationId": {},
      "isClient": true,
      "jobTitle": "string",
      "linkedinUrl": "https://example.com",
      "name": "Ava Chen",
      "source": {},
      "sourceId": {},
      "state": "string",
      "threadUrl": "https://example.com",
      "tiktokUrl": "https://example.com",
      "twitterUrl": "https://example.com",
      "updatedAt": "string",
      "userToBusinessId": {},
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
| `address1` | string |  |
| `address2` | string |  |
| `avatar` | object |  |
| `bgColor` | string |  |
| `brandColour` | string |  |
| `businessId` | string |  |
| `city` | string |  |
| `clientId` | object |  |
| `company` | object |  |
| `companyId` | object |  |
| `country` | string |  |
| `countryCode` | string |  |
| `countryDialCode` | string |  |
| `countryFlag` | string |  |
| `createdAt` | string |  |
| `createdBy.user.fullName` | string |  |
| `createdBy.user.profileImg` | object |  |
| `createdById` | string |  |
| `customSocialMediaUrl` | string |  |
| `facebookUrl` | string |  |
| `fgColor` | string |  |
| `hiddenInCrm` | boolean |  |
| `id` | string |  |
| `industry` | object |  |
| `industryId` | object |  |
| `instagramUrl` | string |  |
| `invitationId` | object |  |
| `isClient` | boolean |  |
| `jobTitle` | string |  |
| `linkedinUrl` | string |  |
| `name` | string |  |
| `source` | object |  |
| `sourceId` | object |  |
| `state` | string |  |
| `threadUrl` | string |  |
| `tiktokUrl` | string |  |
| `twitterUrl` | string |  |
| `updatedAt` | string |  |
| `userToBusinessId` | object |  |
| `youtubeUrl` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `GET /v1/people` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

