# Frontegg: Get Identity Management Configuration

Retrieves identity management configuration from Frontegg.

```
GET https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-identity-management-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frontegg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-identity-management-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/get-identity-management-configuration?${params}`, {
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
      "id": "string",
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
| `id` | string |  |
| `jwtAlgorithm` | string |  |
| `jwtSecret` | string |  |
| `machineToMachineAuthStrategy` | string |  |
| `publicKey` | string |  |
| `refreshTokensRotationLimit` | number |  |
| `rotateRefreshTokens` | boolean |  |

## Native endpoint

Through the native Frontegg API, this operation is `GET /identity/resources/configurations/v1` (base URL `https://api.frontegg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-identity-management-configuration.md) for the provider-specific parameters and requirements.

