# Teachlr Organizations: Get User by Email



```
GET https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Teachlr Organizations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-email?connectionId=$CONNECTION_ID&email=apps%40mindcloud.co" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "apps@mindcloud.co"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teachlrOrganizations/latest/actions/get-user-by-email?${params}`, {
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
| `email` | string | yes | Email address of the Teachlr user to retrieve. Default: `apps@mindcloud.co`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "about": {},
      "agreeTerms": true,
      "agreeTermsAt": {},
      "alternativeId": {},
      "city": {},
      "country": {},
      "countryIsoCode": {},
      "createdAt": "string",
      "department": {},
      "email": "ava@example.com",
      "employeeNumber": "string",
      "externalId": "string",
      "firstLoginAt": {},
      "id": 1,
      "identificationNumber": {},
      "job": {},
      "language": "string",
      "lastActivityAt": {},
      "lastLoginAt": {},
      "lastName": "Chen",
      "name": "Ava Chen",
      "numVisit": 1,
      "organizationId": 1,
      "organizationName": {},
      "phone": {},
      "picture": {
        "large": "string",
        "medium": "string",
        "small": "string",
        "thumb": "string"
      },
      "registerType": "string",
      "subscriber": true,
      "tempEmail": true,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `about` | object |  |
| `agreeTerms` | boolean |  |
| `agreeTermsAt` | object |  |
| `alternativeId` | object |  |
| `city` | object |  |
| `country` | object |  |
| `countryIsoCode` | object |  |
| `createdAt` | string |  |
| `department` | object |  |
| `email` | string |  |
| `employeeNumber` | string |  |
| `externalId` | string |  |
| `firstLoginAt` | object |  |
| `id` | number |  |
| `identificationNumber` | object |  |
| `job` | object |  |
| `language` | string |  |
| `lastActivityAt` | object |  |
| `lastLoginAt` | object |  |
| `lastName` | string |  |
| `name` | string |  |
| `numVisit` | number |  |
| `organizationId` | number |  |
| `organizationName` | object |  |
| `phone` | object |  |
| `picture.large` | string |  |
| `picture.medium` | string |  |
| `picture.small` | string |  |
| `picture.thumb` | string |  |
| `registerType` | string |  |
| `subscriber` | boolean |  |
| `tempEmail` | boolean |  |
| `username` | string |  |

## Native endpoint

Through the native Teachlr Organizations API, this operation is `GET /users/query` (base URL `https://api.teachlr.com/mindcloudteachlr337933/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-email.md) for the provider-specific parameters and requirements.

