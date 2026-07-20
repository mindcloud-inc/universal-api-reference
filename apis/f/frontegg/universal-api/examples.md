# Frontegg Universal API Examples

These examples use the MindCloud API key and Frontegg connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Identity Management Configuration

Retrieves identity management configuration from Frontegg.

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

Example response:

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

See the full [Get Identity Management Configuration action reference](actions/get-identity-management-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/frontegg/latest/actions/get-identity-management-configuration).

## Add Roles To Group

Adds roles to a user group in Frontegg.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/add-roles-to-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "roleIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frontegg/latest/actions/add-roles-to-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "roleIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Roles To Group action reference](actions/add-roles-to-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/frontegg/latest/actions/add-roles-to-group).
