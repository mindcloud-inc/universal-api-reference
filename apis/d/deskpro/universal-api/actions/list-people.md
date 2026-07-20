# Deskpro: List People

Retrieves a list of people from Deskpro.

```
GET https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-people
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deskpro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskpro/latest/actions/list-people?${params}`, {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentData.agentCallsEnabled` | boolean |  |
| `agentData.agentCanUseForwarding` | boolean |  |
| `agentData.agentChatEnabled` | boolean |  |
| `agentData.agentType` | string |  |
| `agentData.availableStatus` | string |  |
| `agentData.forwardingLoggedOut` | boolean |  |
| `agentData.forwardingNumber` | string |  |
| `agentData.forwardingNumberType` | string |  |
| `agentData.forwardingRingTimeout` | number |  |
| `agentData.lastOnline` | date |  |
| `agentData.loginStatus` | string |  |
| `agentData.workStatusEnabled` | boolean |  |
| `agentGroups[]` | number |  |
| `allUserGroups[]` | number |  |
| `avatar.defaultUrlPattern` | string |  |
| `brands[]` | number |  |
| `canAdmin` | boolean |  |
| `canAgent` | boolean |  |
| `canBilling` | boolean |  |
| `canReopenResolved.permission` | boolean |  |
| `canReports` | boolean |  |
| `chatsCount` | number |  |
| `creationSystem` | string |  |
| `dateCreated` | date |  |
| `dateLastLogin` | date |  |
| `disableAutoresponses` | boolean |  |
| `disablePicture` | boolean |  |
| `displayContact` | string |  |
| `displayName` | string |  |
| `emails[]` | string |  |
| `firstName` | string |  |
| `gravatarUrl` | string |  |
| `id` | number |  |
| `isAgent` | boolean |  |
| `isConfirmed` | boolean |  |
| `isContact` | boolean |  |
| `isDeleted` | boolean |  |
| `isDisabled` | boolean |  |
| `isUser` | boolean |  |
| `language` | number |  |
| `lastName` | string |  |
| `lastSeen` | date |  |
| `name` | string |  |
| `online` | boolean |  |
| `onlineForChat` | boolean |  |
| `organizationManager` | boolean |  |
| `organizationPosition` | string |  |
| `overrideDisplayName` | string |  |
| `primaryEmail` | string |  |
| `primaryTeam` | number |  |
| `summary` | string |  |
| `teams[]` | number |  |
| `ticketsCount` | number |  |
| `timelimit` | number |  |
| `timezone` | string |  |
| `titlePrefix` | string |  |
| `wasAgent` | boolean |  |

## Native endpoint

Through the native Deskpro API, this operation is `GET /people` (base URL `{{credentials.helpdeskUrl}}/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-people.md) for the provider-specific parameters and requirements.

