# OneSuite: Convert Company to Client

Converts a company to a client in OneSuite.

```
PUT https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/convert-company-to-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/convert-company-to-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "cmo7gu3gq02robo05g27zy4n0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/convert-company-to-client', {
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
| `companyId` | string | yes | Company ID from the OneSuite convert-company docs. Example: `cmo7gu3gq02robo05g27zy4n0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Optional invitation message for invited people. Example: `Welcome to our client portal!`. |
| `invitePeopleIds[]` | array<string> | no | Optional list of people IDs to invite to the client portal. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
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
        "industryId": {},
        "instagramUrl": "https://example.com",
        "isClient": true,
        "linkedinUrl": "https://example.com",
        "logo": {},
        "name": "Ava Chen",
        "pointOfContactId": {},
        "sourceId": {},
        "state": "string",
        "threadUrl": "https://example.com",
        "tiktokUrl": "https://example.com",
        "twitterUrl": "https://example.com",
        "updatedAt": "string",
        "youtubeUrl": "https://example.com",
        "zip": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.accountOwnerId` | object |  |
| `data.address1` | string |  |
| `data.address2` | string |  |
| `data.annualRecurringRevenue` | number |  |
| `data.bgColor` | string |  |
| `data.brandColour` | string |  |
| `data.businessId` | string |  |
| `data.city` | string |  |
| `data.country` | string |  |
| `data.countryCode` | string |  |
| `data.countryDialCode` | string |  |
| `data.countryFlag` | string |  |
| `data.createdAt` | string |  |
| `data.createdById` | string |  |
| `data.currency` | string |  |
| `data.currencyName` | string |  |
| `data.currencySymbol` | string |  |
| `data.customSocialMediaUrl` | string |  |
| `data.employees` | number |  |
| `data.facebookUrl` | string |  |
| `data.fgColor` | string |  |
| `data.hiddenInCrm` | boolean |  |
| `data.icp` | boolean |  |
| `data.id` | string |  |
| `data.industryId` | object |  |
| `data.instagramUrl` | string |  |
| `data.isClient` | boolean |  |
| `data.linkedinUrl` | string |  |
| `data.logo` | object |  |
| `data.name` | string |  |
| `data.pointOfContactId` | object |  |
| `data.sourceId` | object |  |
| `data.state` | string |  |
| `data.threadUrl` | string |  |
| `data.tiktokUrl` | string |  |
| `data.twitterUrl` | string |  |
| `data.updatedAt` | string |  |
| `data.youtubeUrl` | string |  |
| `data.zip` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `POST /v1/companies/:company_id/convert-to-client` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-company-to-client.md) for the provider-specific parameters and requirements.

