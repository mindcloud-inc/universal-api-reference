# Tally Universal API Examples

These examples use the MindCloud API key and Tally connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info



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

Example response:

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

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tally/latest/actions/get-user-info).

## Create Invite



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tally/latest/actions/create-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "workspaceIds": "string",
  "emails": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tally/latest/actions/create-invite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "workspaceIds": "string",
    "emails": "ava@example.com"
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

See the full [Create Invite action reference](actions/create-invite.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tally/latest/actions/create-invite).
