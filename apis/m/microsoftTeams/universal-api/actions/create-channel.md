# Microsoft Teams: Create Channel

Creates a new channel in Microsoft Teams.

```
POST https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "displayName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/create-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "displayName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | Microsoft Graph team ID. |
| `displayName` | string | yes | Channel display name. |
| `description` | string | no | Optional channel description. |
| `membershipType` | string | no | Channel membership type. Use standard, private, or shared. Default: `standard`. |

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

Through the native Microsoft Teams API, this operation is `POST /v1.0/teams/:teamId/channels` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-channel.md) for the provider-specific parameters and requirements.

