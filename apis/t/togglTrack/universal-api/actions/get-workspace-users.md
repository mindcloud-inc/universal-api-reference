# Toggl Track: Get Workspace Users

Retrieves workspace users from Toggl Track.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-workspace-users?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/get-workspace-users?${params}`, {
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
| `workspaceId` | list<number> | yes |  |
| `excludeDeleted` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "id": 1,
      "inactive": true,
      "isActive": true,
      "isAdmin": true,
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fullname` | string |  |
| `id` | number |  |
| `inactive` | boolean |  |
| `isActive` | boolean |  |
| `isAdmin` | boolean |  |
| `role` | string |  |

## Native endpoint

Through the native Toggl Track API, this operation is `GET /api/v9/workspaces/:workspace_id/users` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workspace-users.md) for the provider-specific parameters and requirements.

