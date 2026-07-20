# HelpDesk: List Teams

Retrieves teams from HelpDesk.

```
GET https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-teams?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "ID": "string",
      "integrations": {},
      "licenseID": 1,
      "name": "Ava Chen",
      "replyAddressID": "string",
      "replyName": "Ava Chen",
      "settings": {
        "notifyTeamAboutAssignedTicket": true,
        "notifyTeamAboutRequestersActivity": true,
        "tagReminder": true,
        "unauthReplyCreatesNewTicket": true
      },
      "templateID": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `createdByType` | string |  |
| `ID` | string |  |
| `integrations` | object |  |
| `licenseID` | number |  |
| `name` | string |  |
| `replyAddressID` | string |  |
| `replyName` | string |  |
| `settings` | object |  |
| `settings.notifyTeamAboutAssignedTicket` | boolean |  |
| `settings.notifyTeamAboutRequestersActivity` | boolean |  |
| `settings.tagReminder` | boolean |  |
| `settings.unauthReplyCreatesNewTicket` | boolean |  |
| `templateID` | string |  |
| `updatedAt` | date |  |
| `updatedBy` | string |  |

## Native endpoint

Through the native HelpDesk API, this operation is `GET /v1/teams` (base URL `https://api.helpdesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

