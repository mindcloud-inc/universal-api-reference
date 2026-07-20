# Deskpro Universal API Examples

These examples use the MindCloud API key and Deskpro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Deskpro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-current-user?${params}`, {
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
      "apiVersion": 1,
      "authMethod": "string",
      "clientType": "string",
      "clientVersion": "string",
      "person": {
        "agentData": {
          "agentCallsEnabled": true,
          "agentCanUseForwarding": true,
          "agentChatEnabled": true,
          "agentType": "string",
          "availableStatus": "string",
          "forwardingLoggedOut": true,
          "forwardingNumber": "string",
          "forwardingNumberType": "string",
          "forwardingRingTimeout": 1,
          "lastOnline": "2026-05-07T12:00:00.000Z",
          "loginStatus": "string",
          "workStatusEnabled": true
        },
        "agentGroups": [
          1
        ],
        "allUserGroups": [
          1
        ],
        "avatar": {
          "defaultUrlPattern": "https://example.com"
        },
        "brands": [
          1
        ],
        "canAdmin": true,
        "canAgent": true,
        "canBilling": true,
        "canReopenResolved": {
          "permission": true
        },
        "canReports": true,
        "chatsCount": 1,
        "creationSystem": "string",
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "dateLastLogin": "2026-05-07T12:00:00.000Z",
        "disableAutoresponses": true,
        "disablePicture": true,
        "displayContact": "string",
        "displayName": "Ava Chen",
        "emails": [
          "ava@example.com"
        ],
        "firstName": "Ava",
        "gravatarUrl": "https://example.com",
        "id": 1,
        "isAgent": true,
        "isConfirmed": true,
        "isContact": true,
        "isDeleted": true,
        "isDisabled": true,
        "isUser": true,
        "language": 1,
        "lastName": "Chen",
        "lastSeen": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "online": true,
        "onlineForChat": true,
        "organizationManager": true,
        "organizationPosition": "string",
        "overrideDisplayName": "Ava Chen",
        "primaryEmail": "ava@example.com",
        "primaryTeam": 1,
        "summary": "string",
        "teams": [
          1
        ],
        "ticketsCount": 1,
        "timelimit": 1,
        "timezone": "string",
        "titlePrefix": "string",
        "wasAgent": true
      },
      "personId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deskpro/latest/actions/get-current-user).
