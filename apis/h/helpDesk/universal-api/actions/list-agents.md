# HelpDesk: List Agents

Retrieves agents from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-agents?${params}`, {
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
      "accountID": "string",
      "autoassignment": true,
      "autoassignmentTeamIDs": [
        "string"
      ],
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailVerified": true,
      "flags": {},
      "ID": "string",
      "jobTitle": "string",
      "licenseID": 1,
      "name": "Ava Chen",
      "organizationOwner": true,
      "roles": [
        "string"
      ],
      "settings": {
        "emailNotificationsActive": true,
        "theme": "string",
        "timeZone": "string"
      },
      "signature": {
        "text": "string"
      },
      "status": "string",
      "teamIDs": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountID` | string |  |
| `autoassignment` | boolean |  |
| `autoassignmentTeamIDs` | array<string> |  |
| `avatar` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `flags` | object |  |
| `ID` | string |  |
| `jobTitle` | string |  |
| `licenseID` | number |  |
| `name` | string |  |
| `organizationOwner` | boolean |  |
| `roles` | array<string> |  |
| `settings` | object |  |
| `settings.emailNotificationsActive` | boolean |  |
| `settings.theme` | string |  |
| `settings.timeZone` | string |  |
| `signature` | object |  |
| `signature.text` | string |  |
| `status` | string |  |
| `teamIDs` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/agents` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

