# Productive.io: List Users

Retrieves users from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-users?${params}`, {
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
      "attributes": {
        "accountAccessExpiresAt": "string",
        "avatarUrl": "https://example.com",
        "defaultOrganizationId": 1,
        "defaultOrganizationSlug": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "icalToken": "string",
        "intercomHash": "string",
        "lastName": "Chen",
        "locale": "string",
        "newsletterConsent": true,
        "newsletterConsentAt": "string",
        "preferences": "string",
        "ssoProvision": true,
        "sysadmin": true,
        "sysadminPermissions": [
          "string"
        ],
        "timeZone": "string",
        "twoFactorAuth": true,
        "updatedAt": "string"
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
| `attributes.accountAccessExpiresAt` | string |  |
| `attributes.avatarUrl` | string |  |
| `attributes.defaultOrganizationId` | number |  |
| `attributes.defaultOrganizationSlug` | string |  |
| `attributes.email` | string |  |
| `attributes.firstName` | string |  |
| `attributes.icalToken` | string |  |
| `attributes.intercomHash` | string |  |
| `attributes.lastName` | string |  |
| `attributes.locale` | string |  |
| `attributes.newsletterConsent` | boolean |  |
| `attributes.newsletterConsentAt` | string |  |
| `attributes.preferences` | string |  |
| `attributes.ssoProvision` | boolean |  |
| `attributes.sysadmin` | boolean |  |
| `attributes.sysadminPermissions` | array<string> |  |
| `attributes.timeZone` | string |  |
| `attributes.twoFactorAuth` | boolean |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /users` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

