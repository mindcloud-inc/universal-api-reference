# CINCEL: Get Team



```
GET https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CINCEL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-team?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cINCEL/latest/actions/get-team?${params}`, {
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
| `uuid` | string | yes | UUID of the team to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "darkLogo": "string",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "emoji": "string",
      "lightLogo": "string",
      "logoUrl": "https://example.com",
      "name": "Ava Chen",
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string",
      "workspace": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Team avatar URL. |
| `createdAt` | date | Team creation timestamp. |
| `darkLogo` | string | Dark theme logo URL. |
| `deletedAt` | date | Deletion timestamp when the team has been deleted. |
| `emoji` | string | Team emoji, when configured. |
| `lightLogo` | string | Light theme logo URL. |
| `logoUrl` | string | Primary team logo URL. |
| `name` | string | Team name. |
| `role` | string | Role of the current user in the team. |
| `updatedAt` | date | Team last update timestamp. |
| `uuid` | string | Unique team UUID. |
| `workspace` | string | Workspace UUID when the team belongs to a workspace. |

## Native endpoint

Through the native CINCEL API, this operation is `GET /teams/:uuid` (base URL `https://api.cincel.digital/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

