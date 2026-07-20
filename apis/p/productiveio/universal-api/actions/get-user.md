# Productive.io: Get User

Retrieves a user from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The Productive resource ID. |

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

Through the native Productive.io API, this operation is `GET /users/{{id}}` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

