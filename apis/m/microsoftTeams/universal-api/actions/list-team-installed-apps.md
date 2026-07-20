# Microsoft Teams: List Team Installed Apps

Retrieves installed apps for a Microsoft Teams team.

```
GET https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-team-installed-apps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Teams `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-team-installed-apps?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftTeams/latest/actions/list-team-installed-apps?${params}`, {
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
| `consentedPermissionSet` | object | Resource-specific permissions consented for the installed app. |
| `id` | string | Unique ID of the Teams app installation. |
| `teamsApp` | object | Related Teams app, when expanded. |
| `teamsAppDefinition` | object | Related Teams app definition, when expanded. |

## Native endpoint

Through the native Microsoft Teams API, this operation is `GET /v1.0/teams/:teamId/installedApps` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-installed-apps.md) for the provider-specific parameters and requirements.

