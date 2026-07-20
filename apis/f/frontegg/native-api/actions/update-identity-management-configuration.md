# Update Identity Management Configuration with Frontegg

Updates identity management configuration in Frontegg.

## Endpoint

- **Method:** `POST`
- **Path:** `/identity/resources/configurations/v1`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [Update Identity Management Configuration](https://developers.frontegg.com/ciam/api/identity/core-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `defaultTokenExpiration` | body | `number` | no | Default access token expiration in seconds. |
| `defaultRefreshTokenExpiration` | body | `number` | no | Default refresh token expiration in seconds. |
| `cookieSameSite` | body | `string` | no | Cookie same-site policy. |
| `machineToMachineAuthStrategy` | body | `string` | no | Machine-to-machine auth strategy. |
| `allowSignups` | body | `boolean` | no | Whether signups are allowed. |
| `apiTokensEnabled` | body | `boolean` | no | Whether API tokens are enabled. |
| `allowOverridePasswordComplexity` | body | `boolean` | no | — |
| `allowOverridePasswordExpiration` | body | `boolean` | no | — |
| `allowOverrideEnforcePasswordHistory` | body | `boolean` | no | — |
| `jwtAlgorithm` | body | `string` | no | JWT signing algorithm. |
| `allowNotVerifiedUsersLogin` | body | `boolean` | no | Whether unverified users can sign in. |
| `forcePermissions` | body | `boolean` | no | Whether permissions are always enforced. |
| `authStrategy` | body | `string` | no | Primary auth strategy. |
| `defaultPasswordlessTokenExpiration` | body | `number` | no | Default passwordless token expiration in seconds. |
| `forceSameDeviceOnAuth` | body | `boolean` | no | Whether auth must continue on the same device. |
| `allowTenantInvitations` | body | `boolean` | no | Whether tenant invitations are allowed. |
| `rotateRefreshTokens` | body | `boolean` | no | Whether refresh tokens rotate. |
| `skipTenantValidation` | body | `boolean` | no | — |
| `addRolesToJwt` | body | `boolean` | no | Whether roles are added to JWTs. |
| `addPermissionsToJwt` | body | `boolean` | no | Whether permissions are added to JWTs. |
| `addSamlAttributesToJwt` | body | `boolean` | no | Whether SAML attributes are added to JWTs. |
| `allowCustomLoginTenantSwitch` | body | `boolean` | no | Whether custom login tenant switching is allowed. |
