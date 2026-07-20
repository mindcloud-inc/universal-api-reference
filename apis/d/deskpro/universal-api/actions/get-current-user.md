# Deskpro: Get Current User

Retrieves the current user from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

## Example request

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



## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiVersion` | number |  |
| `authMethod` | string |  |
| `clientType` | string |  |
| `clientVersion` | string |  |
| `person.agentData.agentCallsEnabled` | boolean |  |
| `person.agentData.agentCanUseForwarding` | boolean |  |
| `person.agentData.agentChatEnabled` | boolean |  |
| `person.agentData.agentType` | string |  |
| `person.agentData.availableStatus` | string |  |
| `person.agentData.forwardingLoggedOut` | boolean |  |
| `person.agentData.forwardingNumber` | string |  |
| `person.agentData.forwardingNumberType` | string |  |
| `person.agentData.forwardingRingTimeout` | number |  |
| `person.agentData.lastOnline` | date |  |
| `person.agentData.loginStatus` | string |  |
| `person.agentData.workStatusEnabled` | boolean |  |
| `person.agentGroups[]` | number |  |
| `person.allUserGroups[]` | number |  |
| `person.avatar.defaultUrlPattern` | string |  |
| `person.brands[]` | number |  |
| `person.canAdmin` | boolean |  |
| `person.canAgent` | boolean |  |
| `person.canBilling` | boolean |  |
| `person.canReopenResolved.permission` | boolean |  |
| `person.canReports` | boolean |  |
| `person.chatsCount` | number |  |
| `person.creationSystem` | string |  |
| `person.dateCreated` | date |  |
| `person.dateLastLogin` | date |  |
| `person.disableAutoresponses` | boolean |  |
| `person.disablePicture` | boolean |  |
| `person.displayContact` | string |  |
| `person.displayName` | string |  |
| `person.emails[]` | string |  |
| `person.firstName` | string |  |
| `person.gravatarUrl` | string |  |
| `person.id` | number |  |
| `person.isAgent` | boolean |  |
| `person.isConfirmed` | boolean |  |
| `person.isContact` | boolean |  |
| `person.isDeleted` | boolean |  |
| `person.isDisabled` | boolean |  |
| `person.isUser` | boolean |  |
| `person.language` | number |  |
| `person.lastName` | string |  |
| `person.lastSeen` | date |  |
| `person.name` | string |  |
| `person.online` | boolean |  |
| `person.onlineForChat` | boolean |  |
| `person.organizationManager` | boolean |  |
| `person.organizationPosition` | string |  |
| `person.overrideDisplayName` | string |  |
| `person.primaryEmail` | string |  |
| `person.primaryTeam` | number |  |
| `person.summary` | string |  |
| `person.teams[]` | number |  |
| `person.ticketsCount` | number |  |
| `person.timelimit` | number |  |
| `person.timezone` | string |  |
| `person.titlePrefix` | string |  |
| `person.wasAgent` | boolean |  |
| `personId` | number |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /me` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

