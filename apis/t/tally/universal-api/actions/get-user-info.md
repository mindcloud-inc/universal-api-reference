# Tally: Get User Info



```
GET https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tally `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tally/latest/actions/get-user-info?${params}`, {
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
      "authenticationMethodsCount": 1,
      "authorizationToken": "string",
      "avatarUrl": "https://example.com",
      "canAccessBilling": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "emailDomain": "ava@example.com",
      "excessUsage": {},
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hasAccess": true,
      "hasPasswordSet": true,
      "hasPendingSubscriptionCancellation": true,
      "hasTwoFactorEnabled": true,
      "id": "string",
      "isBlocked": true,
      "isDeleted": true,
      "isOrganizationOwner": true,
      "isUnknownDeviceVerificationDisabled": true,
      "lastName": "Chen",
      "organizationId": "string",
      "organizationOwner": {
        "authenticationMethodsCount": 1,
        "avatarUrl": "https://example.com",
        "createdAt": "string",
        "email": "ava@example.com",
        "emailDomain": {},
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "hasPasswordSet": true,
        "hasTwoFactorEnabled": true,
        "id": "string",
        "isBlocked": true,
        "isDeleted": true,
        "isUnknownDeviceVerificationDisabled": true,
        "lastName": "Chen",
        "organizationId": "string",
        "ssoIsConnectedWithApple": true,
        "ssoIsConnectedWithGoogle": true,
        "timezone": "string",
        "updatedAt": "string"
      },
      "ssoIsConnectedWithApple": true,
      "ssoIsConnectedWithGoogle": true,
      "subscriptionPlan": "string",
      "timezone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticationMethodsCount` | number |  |
| `authorizationToken` | string |  |
| `avatarUrl` | string |  |
| `canAccessBilling` | boolean |  |
| `createdAt` | string |  |
| `email` | string |  |
| `emailDomain` | string |  |
| `excessUsage` | object |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `hasAccess` | boolean |  |
| `hasPasswordSet` | boolean |  |
| `hasPendingSubscriptionCancellation` | boolean |  |
| `hasTwoFactorEnabled` | boolean |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `isDeleted` | boolean |  |
| `isOrganizationOwner` | boolean |  |
| `isUnknownDeviceVerificationDisabled` | boolean |  |
| `lastName` | string |  |
| `organizationId` | string |  |
| `organizationOwner.authenticationMethodsCount` | number |  |
| `organizationOwner.avatarUrl` | string |  |
| `organizationOwner.createdAt` | string |  |
| `organizationOwner.email` | string |  |
| `organizationOwner.emailDomain` | object |  |
| `organizationOwner.firstName` | string |  |
| `organizationOwner.fullName` | string |  |
| `organizationOwner.hasPasswordSet` | boolean |  |
| `organizationOwner.hasTwoFactorEnabled` | boolean |  |
| `organizationOwner.id` | string |  |
| `organizationOwner.isBlocked` | boolean |  |
| `organizationOwner.isDeleted` | boolean |  |
| `organizationOwner.isUnknownDeviceVerificationDisabled` | boolean |  |
| `organizationOwner.lastName` | string |  |
| `organizationOwner.organizationId` | string |  |
| `organizationOwner.ssoIsConnectedWithApple` | boolean |  |
| `organizationOwner.ssoIsConnectedWithGoogle` | boolean |  |
| `organizationOwner.timezone` | string |  |
| `organizationOwner.updatedAt` | string |  |
| `ssoIsConnectedWithApple` | boolean |  |
| `ssoIsConnectedWithGoogle` | boolean |  |
| `subscriptionPlan` | string |  |
| `timezone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Tally API, this operation is `GET https://api.tally.so/users/me` (base URL `https://api.tally.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

