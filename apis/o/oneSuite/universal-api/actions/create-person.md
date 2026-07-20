# OneSuite: Create Person

Creates a person in OneSuite.

```
POST https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-person" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Jane Doe"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/create-person', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Jane Doe"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Full name of the person from the official create-people docs. Example: `Jane Doe`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | string | no | Optional company ID to associate with the person at creation time. Example: `cmo7gu3gq02robo05g27zy4n0`. |

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

Through the native OneSuite API, this operation is `POST /v2/people` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-person.md) for the provider-specific parameters and requirements.

