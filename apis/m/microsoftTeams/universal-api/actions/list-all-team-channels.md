# Microsoft Teams: List All Team Channels

Retrieves all team channels from Microsoft Teams.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-all-team-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-all-team-channels?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-all-team-channels?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "isArchived": true,
      "isFavoriteByDefault": true,
      "membershipType": "string",
      "tenantId": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date | Read-only timestamp at which the channel was created. |
| `description` | string | Optional textual description for the channel. |
| `displayName` | string | Channel name as it appears in Microsoft Teams. |
| `email` | string | Read-only email address for sending messages to the channel. |
| `id` | string | Read-only unique identifier for the channel. |
| `isArchived` | boolean | Whether the channel is archived. |
| `isFavoriteByDefault` | boolean | Whether the channel is recommended by default. |
| `membershipType` | string | Type of channel membership. |
| `tenantId` | string | Microsoft Entra tenant identifier. |
| `webUrl` | string | Opaque Microsoft Teams client URL for the channel. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/teams/:teamId/allChannels` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-team-channels.md) for the provider-specific parameters and requirements.

