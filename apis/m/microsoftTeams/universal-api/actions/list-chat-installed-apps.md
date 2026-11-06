# Microsoft Teams: List Chat Installed Apps

Retrieves installed apps for a Microsoft Teams chat.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-chat-installed-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-chat-installed-apps?connectionId=$CONNECTION_ID&chatId=19%3Aabc123%40thread.v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chatId": "19:abc123@thread.v2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-chat-installed-apps?${params}`, {
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
| `chatId` | string | yes | Microsoft Teams chat ID. Example: `19:abc123@thread.v2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consentedPermissionSet": {},
      "id": "string",
      "teamsApp": {},
      "teamsAppDefinition": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consentedPermissionSet` | object | Resource-specific permissions consented for the installation, when present. |
| `id` | string | Unique identifier for the Teams app installation in the chat. |
| `teamsApp` | object | Teams app associated with the installation when expanded. |
| `teamsAppDefinition` | object | Teams app definition associated with the installation when expanded. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/chats/:chatId/installedApps` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-installed-apps.md) for the provider-specific parameters and requirements.

