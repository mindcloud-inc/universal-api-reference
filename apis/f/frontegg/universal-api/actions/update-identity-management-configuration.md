# Frontegg: Update Identity Management Configuration

Updates identity management configuration in Frontegg.

```
PUT https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-identity-management-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-identity-management-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/update-identity-management-configuration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `defaultTokenExpiration` | number | no | Default access token expiration in seconds. |
| `defaultRefreshTokenExpiration` | number | no | Default refresh token expiration in seconds. |
| `cookieSameSite` | string | no | Cookie same-site policy. |
| `machineToMachineAuthStrategy` | string | no | Machine-to-machine auth strategy. |
| `allowSignups` | boolean | no | Whether signups are allowed. |
| `apiTokensEnabled` | boolean | no | Whether API tokens are enabled. |
| `allowOverridePasswordComplexity` | boolean | no |  |
| `allowOverridePasswordExpiration` | boolean | no |  |
| `allowOverrideEnforcePasswordHistory` | boolean | no |  |
| `jwtAlgorithm` | string | no | JWT signing algorithm. |
| `allowNotVerifiedUsersLogin` | boolean | no | Whether unverified users can sign in. |
| `forcePermissions` | boolean | no | Whether permissions are always enforced. |
| `authStrategy` | string | no | Primary auth strategy. |
| `defaultPasswordlessTokenExpiration` | number | no | Default passwordless token expiration in seconds. |
| `forceSameDeviceOnAuth` | boolean | no | Whether auth must continue on the same device. |
| `allowTenantInvitations` | boolean | no | Whether tenant invitations are allowed. |
| `rotateRefreshTokens` | boolean | no | Whether refresh tokens rotate. |
| `skipTenantValidation` | boolean | no |  |
| `addRolesToJwt` | boolean | no | Whether roles are added to JWTs. |
| `addPermissionsToJwt` | boolean | no | Whether permissions are added to JWTs. |
| `addSamlAttributesToJwt` | boolean | no | Whether SAML attributes are added to JWTs. |
| `allowCustomLoginTenantSwitch` | boolean | no | Whether custom login tenant switching is allowed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addPermissionsToJwt": true,
      "addRolesToJwt": true,
      "addSamlAttributesToJwt": true,
      "allowCustomLoginTenantSwitch": true,
      "allowNotVerifiedUsersLogin": true,
      "allowOverrideEnforcePasswordHistory": true,
      "allowOverridePasswordComplexity": true,
      "allowOverridePasswordExpiration": true,
      "allowSignups": true,
      "allowTenantInvitations": true,
      "apiTokensEnabled": true,
      "authStrategy": "string",
      "cookieSameSite": "string",
      "defaultPasswordlessTokenExpiration": 1,
      "defaultRefreshTokenExpiration": 1,
      "defaultTokenExpiration": 1,
      "forcePermissions": true,
      "forceSameDeviceOnAuth": true,
      "jwtAlgorithm": "string",
      "jwtSecret": "string",
      "machineToMachineAuthStrategy": "string",
      "publicKey": "string",
      "refreshTokensRotationLimit": 1,
      "rotateRefreshTokens": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addPermissionsToJwt` | boolean |  |
| `addRolesToJwt` | boolean |  |
| `addSamlAttributesToJwt` | boolean |  |
| `allowCustomLoginTenantSwitch` | boolean |  |
| `allowNotVerifiedUsersLogin` | boolean |  |
| `allowOverrideEnforcePasswordHistory` | boolean |  |
| `allowOverridePasswordComplexity` | boolean |  |
| `allowOverridePasswordExpiration` | boolean |  |
| `allowSignups` | boolean |  |
| `allowTenantInvitations` | boolean |  |
| `apiTokensEnabled` | boolean |  |
| `authStrategy` | string |  |
| `cookieSameSite` | string |  |
| `defaultPasswordlessTokenExpiration` | number |  |
| `defaultRefreshTokenExpiration` | number |  |
| `defaultTokenExpiration` | number |  |
| `forcePermissions` | boolean |  |
| `forceSameDeviceOnAuth` | boolean |  |
| `jwtAlgorithm` | string |  |
| `jwtSecret` | string |  |
| `machineToMachineAuthStrategy` | string |  |
| `publicKey` | string |  |
| `refreshTokensRotationLimit` | number |  |
| `rotateRefreshTokens` | boolean |  |

## Native endpoint

Through the native Frontegg API, this operation is `POST /identity/resources/configurations/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-identity-management-configuration.md) for the provider-specific parameters and requirements.

