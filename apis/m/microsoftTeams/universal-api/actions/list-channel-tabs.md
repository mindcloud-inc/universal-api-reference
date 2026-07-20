# Microsoft Teams: List Channel Tabs

Retrieves channel tabs from Microsoft Teams.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-tabs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-tabs?connectionId=$CONNECTION_ID&teamId=string&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-channel-tabs?${params}`, {
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
      "configuration": {},
      "displayName": "Ava Chen",
      "id": "string",
      "sortOrder": 1,
      "teamsApp": {},
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object | Tab configuration settings. |
| `displayName` | string | Name of the tab. |
| `id` | string | Unique identifier for the Teams tab. |
| `sortOrder` | number | Position of the tab in the channel. |
| `teamsApp` | object | Teams app linked to the tab. |
| `webUrl` | string | Deep link URL of the tab. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/teams/:teamId/channels/:channelId/tabs` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-channel-tabs.md) for the provider-specific parameters and requirements.

