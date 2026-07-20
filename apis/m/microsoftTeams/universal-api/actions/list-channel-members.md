# Microsoft Teams: List Channel Members

Retrieves channel members from Microsoft Teams.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-members?connectionId=$CONNECTION_ID&teamId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-members?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Microsoft Graph team ID. |
| `channelId` | string | yes | Microsoft Graph channel ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "displayName": "Ava Chen",
      "id": "string",
      "roles": [
        "string"
      ],
      "visibleHistoryStartDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `displayName` | string | Display name of the user. |
| `id` | string | Read-only unique identifier of the conversation member. |
| `roles` | array<string> | Roles for the user in the conversation. |
| `visibleHistoryStartDateTime` | date | Timestamp denoting how far back conversation history is shared with the member. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/teams/:teamId/channels/:channelId/members` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-members.md) for the provider-specific parameters and requirements.

