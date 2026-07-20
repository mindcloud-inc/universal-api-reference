# Toggl Track: List Tags

Retrieves tags from a Toggl Track workspace.

```
GET https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toggl Track `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-tags?connectionId=$CONNECTION_ID&workspaceId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/togglTrack/latest/actions/list-tags?${params}`, {
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
| `page` | number | no |  |
| `perPage` | number | no |  |
| `search` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "at": "string",
      "creatorId": 1,
      "id": 1,
      "name": "Ava Chen",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `at` | string | Last updated timestamp |
| `creatorId` | number | Creator user ID |
| `id` | number | Tag ID |
| `name` | string | Tag name |
| `workspaceId` | number | Workspace ID |

## Native endpoint

Through the native Toggl Track API, this operation is `GET /api/v9/workspaces/:workspace_id/tags` (base URL `https://api.track.toggl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

