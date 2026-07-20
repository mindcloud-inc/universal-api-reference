# Twist: Get Workspace

Retrieves a workspace from Twist by ID.

```
GET https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-workspace?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twist/latest/actions/get-workspace?${params}`, {
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
| `workspaceId` | number | yes | The id of the workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarUrls": {
        "s195": "https://example.com",
        "s35": "https://example.com",
        "s60": "https://example.com",
        "s640": "https://example.com"
      },
      "color": 1,
      "createdTs": 1,
      "creator": 1,
      "defaultChannel": 1,
      "defaultConversation": 1,
      "id": 1,
      "name": "Ava Chen",
      "plan": "string",
      "security": {
        "guestsSupported": true,
        "usersCanInstallIntegrations": true,
        "usersCanInvite": true
      },
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarUrls.s195` | string |  |
| `avatarUrls.s35` | string |  |
| `avatarUrls.s60` | string |  |
| `avatarUrls.s640` | string |  |
| `color` | number |  |
| `createdTs` | number |  |
| `creator` | number |  |
| `defaultChannel` | number |  |
| `defaultConversation` | number |  |
| `id` | number |  |
| `name` | string |  |
| `plan` | string |  |
| `security.guestsSupported` | boolean |  |
| `security.usersCanInstallIntegrations` | boolean |  |
| `security.usersCanInvite` | boolean |  |
| `version` | number |  |

## Native endpoint

Through the native Twist API, this operation is `GET /workspaces/getone` (base URL `https://api.twist.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace.md) for the provider-specific parameters and requirements.

